# Feels like we only go backwards
Author: shady

Category: Reverse Engineering

Difficulty: Medium

# Description
After finding the backdoor and making your way to the next floor, you step into a chamber awash with shifting colors and swirling echoes, a concert frozen in time. Kevin Parker stands at the center, his riffs bending reality around him. To ascend, you’ll need to join the session on his terms: push your voice further than comfort, align yourself with the number he hides in the haze, and piece together the melody concealed within layers of reverb. Only then will the music open the way upward.

# Mysolve

Really a pain in the ahh challenge. First of all bro i tried to extract the file data in windows. ran it , got ANSI text
then extracted that ANSI text separately thinking that it would become an image..spent an hour or so making the image thinking
id get the flag from there...little did i know.The image i formed (with help chatgpt and claude my goats) was hella blurry but
i could make it out that it looked like tameimpala's "Currents"'s album cover. At the header it has stuff written in yellow so i thought 
that was the flag. THEN...i SAW THE..ORIGINAL ALBUM ART....AND GUESS WAHAT RAHAHHA NO FLAG. i was literally wasting my time on NOTHING.
Then i saw my friend running the ELF file in his lappy. "Oh shit...wsl.."  i thought to myself and launched.
There it was. The tameimapala coverart..staring me down...
And then the quiz started. First question was "kevin wants you to sing your heart out, it could be some music to walk home by:"
Fair enough i tried (my friend tried): "Music To Walk Home By"<tame impala song> gladly it worked.
Level2:it's time for some mind mischief! what number is kevin parker thinking of right now:
So yeah for this we thought that this might be a little different challange , maybe a hard quiz you can only answer by observing
So we tried...The number of tameimpala references so far, Currents release year, Mind Mischief release year listened to couple of
songs on the side.
My teammate was apparently trying to radare2 on the ELF file. Fair enough it worked. He deocded the number 
"8168008136" Gladly it worked.
He was using docker on macOS and then he ran into an issue where his laptop turned and poof data gone.

Cracking the number "8168008136" we started relating it to tameimpala to understand the logic of this answer..
but then i saw it..yes i did...right there hidden in the number..I know you see it too, Those "calcium cannons".
Awh man figured out it was a troll and we really had to use a tool to figure it out.
After that i used the IDA decompiler-disassembler 
1. opened the binary in IDA 
2.Found the "main" function sub_14C0
3. F5 to decompile
level 1 : sub_14C0
level 2 : sub_1340
level 3: sub_1240

apparently my teammate cracked that the flag was 37char long
Extracted the hardcoded arrays from memory of level 3 it
they were stored in hex in binary data section
Loaded the hex into claude (my goat) got the code , ran it got the flag.
Honestly a roller Coaster, Actively took the most time i think after "Case Sensitivity"


Code:
# Flag decoder for the Tame Impala challenge

# v6 array - Complete data from hex dump
# From 0x2330 to end, we need 74 bytes (37 words)
v6_bytes = [
    # 0x2330-0x233F
    0xC9, 0x00, 0xDE, 0x00, 0xFD, 0x00, 0xE0, 0x00, 0xE7, 0x00, 0xEA, 0x00, 0xF9, 0x00, 0x20, 0x01,
    # 0x2340-0x234F
    0xFF, 0x00, 0x9C, 0x00, 0x21, 0x01, 0xFC, 0x00, 0x9F, 0x00, 0x24, 0x01, 0xB7, 0x00, 0x18, 0x01,
    # 0x2350-0x235F
    0x35, 0x01, 0xBC, 0x00, 0x41, 0x01, 0xCC, 0x00, 0x2D, 0x01, 0x48, 0x01, 0xD9, 0x00, 0x64, 0x01,
    # 0x2360-0x236F
    0x5F, 0x01, 0x42, 0x01, 0xEF, 0x00, 0x54, 0x01, 0x5D, 0x01, 0x00, 0x01, 0x75, 0x01, 0x60, 0x01,
    # Continuation at 0x2390 - last 10 bytes (5 words)
    0x8F, 0x01, 0x1C, 0x01, 0x83, 0x01, 0x1C, 0x01, 0x01, 0x1B
]

# Convert bytes to 16-bit words (little endian)
v6 = []
for i in range(0, len(v6_bytes), 2):
    word = v6_bytes[i] | (v6_bytes[i+1] << 8)
    v6.append(word)

print(f"v6 array has {len(v6)} words")

# si128 array - exact bytes from hex dump at 0x2370 and 0x2380
# We need exactly 37 bytes total
# 0x2370: 03 07 0B 0F 0B 07 03 07 0B 0F 0B 07 03 07 0B 0F (16 bytes)
# 0x2380: 0B 07 03 07 0B 0F 0B 07 03 07 0B 0F 0B 07 03 07 (16 bytes)
# Plus 5 more bytes from somewhere - let me check the decompiled code pattern
# The code shows: v5[0].m128i_i64[1] + 5 = 0x3070B0F0B070307LL
# That's bytes: 07 03 07 0B 0F 0B 07 03 (in little endian)

si128 = [
    # First 16 bytes from 0x2370
    0x03, 0x07, 0x0B, 0x0F, 0x0B, 0x07, 0x03, 0x07, 0x0B, 0x0F, 0x0B, 0x07, 0x03, 0x07, 0x0B, 0x0F,
    # Next 16 bytes from 0x2380
    0x0B, 0x07, 0x03, 0x07, 0x0B, 0x0F, 0x0B, 0x07, 0x03, 0x07, 0x0B, 0x0F, 0x0B, 0x07, 0x03, 0x07,
    # Last 5 bytes - continuing the pattern
    0x0B, 0x0F, 0x0B, 0x07, 0x03
]

print(f"si128 array has {len(si128)} bytes")

# Decode the flag using the formula: flag[i] = (v6[i] - si128[i] - 5*i) / 2
flag = []
for i in range(min(len(v6), 37)):
    char_value = (v6[i] - si128[i] - 5*i) // 2
    if 0 <= char_value <= 127:  # Valid ASCII
        flag.append(chr(char_value))
    else:
        flag.append('?')
        print(f"Warning: Invalid character at position {i}: value={char_value}")

flag_string = ''.join(flag)

print("=" * 50)
print("DECODED FLAG:")
print("=" * 50)
print(flag_string)
print("=" * 50)
print()
print(f"Length: {len(flag_string)} characters (expected 37)")

## Output:
S C:\Users\garri\Downloads> python see.py
v6 array has 37 words
si128 array has 37 bytes
Warning: Invalid character at position 36: value=3365
==================================================
DECODED FLAG:
==================================================
citadel{f0r_0n3_m0r3_h0ur_1_c4n_r4g3?
==================================================

Length: 37 characters (expected 37)

yeah so just replaced "?" our dear "}"
