Hello Students

- what happened in the class so far
- what happened in editing class
	- see if any of it ties into what im saying in some way

# Context Setting

- so far, your experimentation has mostly been 
	- record
	- put into audacity
	- layer, superimpose, mix, etc etc
- while great, theres a lot more that you can go into this
in this lecture, we are going to go into all of that.


# Start

the next hour or so is going to be super information dense, but everything important you need to know is what I am gonna say in the next five minutes. 
- diff majors, diff proficiency, that okay, stop, ask questions, no hurry, no worry.
- if you are worried about quiz, dont worry. everything in the quiz will be done in the enxt 10 minutes, rest is just examples.

So what I want to do is basically give you a lot of choice. The way that we have done things in this class so far, is one way to do things. and its useful because there needs to be some entry point somewhere. But, now that we are somewhat comfortable with what we are doing here, and some of you are starting to hit limits with what you want to do vs what you can do, i wish to expand your repertoire a little, remove your constraints.

So to do this, i want to explain to you certain things. 
First we will talk about sound itself, and how it works in the physcial world, then I want to talk to you about how we are working with sound in the computer, and then we will see where it goes.

1. The nature of sound in 
	1. biology
	2. physics
	3. electric
	4. electronic/digital/computer
2. technical mastery vs "vibe", artifacts, "clean sound"
3. choices made for you vs choices you can make
4. i also want to speak a bit about the quest for clean/hi-fi and how that might not always be a good thing or creatively advantageous, eg vinyl, lofi aesthetic, 8 bit sound, etc


### The Three Key Takeaways



1. **You can intervene ANYWHERE in the process** — not just in editing software
2. **Every step is a creative choice** — mic placement, room acoustics, file format, even "mistakes"
3. **Understanding = control** — "limitations" become tools

So what we are going to do, is go through the entire chain of sound, opening the blackbox

BIOLOGY/PHYSICS → ANALOG/ELECTRIC → DIGITAL → ANALOG → PHYSICS


Quick primer on sound physics and biology, 

**BIOLOGY/PHYSICS (the real world)**

- Actual vibrations moving through air, water, solid objects
- This is the physical phenomenon of sound
- It exists whether we record it or not

**First Arrow → ANALOG/ELECTRIC**

- This is transduction—converting physical energy into electrical energy
- Happens in microphones, contact mics, pickups
- Continuous signal (infinite resolution in theory)

**Second Arrow → DIGITAL**

- This is ADC (Analog-to-Digital Conversion)
- Converts continuous voltage into discrete numbers
- Creates a "snapshot" representation of the sound
- This is where sample rate and bit depth come in

**Third Arrow → ANALOG**

- This is DAC (Digital-to-Analog Conversion)
- Converts numbers back into voltage
- Happens in your audio interface, phone, laptop

**Fourth Arrow → PHYSICS**

- Voltage drives a speaker/transducer
- Speaker vibrates air
- Sound becomes physical phenomenon again
- Reaches your ears (which transduce it AGAIN into neural signals, but that's beyond our scope)


### Context: Why This Matters - Extended Discussion

**The Dominant Paradigm:**

Most of the discourse around recording—especially online, especially on forums, especially in 'how to' videos—is about technical perfection:

- _Cleanest signal possible_
- _Lowest noise floor_
- _Most expensive gear_
- _'Transparent' recording_

_And look, that's ONE valid approach. If you're recording a symphony orchestra, you probably want that. But it's not the ONLY approach.

**The Counter-Examples:**

_"Think about these sounds:_

- **Vinyl crackle and warmth** - literally artifacts of the medium (dust, physical degradation, mechanical imperfections)
- **8-bit/chiptune sound** - the limitations of early gaming hardware, now an aesthetic choice
- **Cassette tape warble** - mechanical instability, now nostalgia
- **Phone recordings** - compressed, thin, but incredibly intimate and immediate
- **AM radio** - limited bandwidth, but evocative of a specific time/place*

**The Black Box Problem:**

_"Here's the thing about your phone or laptop as a recording device:_

_When you hit 'record' on your phone, here's what's actually happening:_

1. Built-in mic captures sound (probably a cheap electret mic)
2. Mic signal goes to a preamp (you can't control the gain)
3. Preamp goes to ADC (you can't choose sample rate or bit depth, it's decided by the OS)
4. Signal gets processed by algorithms (noise reduction, automatic gain control, compression—all happening invisibly)
5. Gets encoded to a file format (probably compressed)
6. Stored in memory

_You have basically ZERO control over any of that. It's a black box._

_TODAY, we're opening that black box. We're going to understand each step so you can make INTENTIONAL choices instead of accepting whatever defaults Apple or Samsung decided for you.

## **SEGMENT 2: What IS Sound?** (3 min)

### Physics Basics - Full Explanation

_"Before we talk about recording sound, we need to understand what sound IS at a physical level. Don't worry, this won't be a physics lecture, just the essentials."_

**Sound as Vibration:**

_"Sound is a MECHANICAL WAVE—it's the physical vibration of particles in a medium. That medium can be:_

- _Air (most common for hearing)_
- _Water (whales, submarines, hydrophones)_
- _Solids (put your ear to a table and tap the other end)_

_Sound CANNOT travel through a vacuum. No medium = no sound. That's why space is silent—there's no air for vibrations to travel through._

_When something vibrates—a guitar string, a speaker cone, your vocal cords—it pushes and pulls on the air molecules around it, creating areas of compression (high pressure) and rarefaction (low pressure). These pressure waves propagate outward until they hit something—like your eardrum or a microphone."_

**The Three Properties of Sound:**

**1. FREQUENCY (Pitch)**

- How many vibrations per second (measured in Hertz, Hz)
- 20 Hz = very low bass (threshold of human hearing)
- 440 Hz = A above middle C (standard tuning reference)
- 20,000 Hz (20 kHz) = very high treble (upper limit of human hearing, decreases with age)
- Below 20 Hz = infrasound (you can feel it but not "hear" it)
- Above 20 kHz = ultrasound (bats, dolphins, some animals can hear it)

_"Fast vibrations = high pitch. Slow vibrations = low pitch. Simple as that."_

**2. AMPLITUDE (Volume/Loudness)**

- How much the pressure changes (how far the particles move)
- Measured in decibels (dB), which is a logarithmic scale
- 0 dB SPL = threshold of human hearing (quietest possible sound)
- 30 dB = whisper
- 60 dB = normal conversation
- 85 dB = hearing damage starts with prolonged exposure
- 120 dB = threshold of pain
- 130+ dB = immediate hearing damage

_"Large vibrations = loud sound. Small vibrations = quiet sound."_

**Logarithmic Scale Explanation:** _"Decibels are weird because they're logarithmic. Every 10 dB increase is roughly a doubling of perceived loudness, but it's actually a 10x increase in actual acoustic power. So 80 dB isn't twice as loud as 70 dB—it's 10 times more powerful acoustically, but only sounds about twice as loud to our ears. Our ears are logarithmic sensors."_

**3. TIMBRE (Texture/Color/Quality)**

- What makes a trumpet sound different from a violin even when playing the same note
- Determined by the harmonic content—the overtones and their relative amplitudes
- Also affected by attack, decay, sustain, release (the envelope)

_"This is the 'shape' of the sound wave. A pure sine wave (just the fundamental frequency) sounds smooth and simple—like a tuning fork or old telephone. But most real-world sounds are complex—they have a fundamental frequency PLUS a bunch of overtones (harmonics) that give them character._

_A piano note is actually dozens of frequencies happening at once—the fundamental, plus the 2nd harmonic (octave up), 3rd harmonic, 4th, 5th, all the way up, each at different volumes. THAT complex mixture is what makes it sound like a piano instead of a beep."_



# Variable #1: The Source
**What Vibrates?**

- Human voice (vocal cords)
- Musical instruments (strings, membranes, air columns, metal bars)
- Found sounds (doors creaking, footsteps, wind, rain)
- Electronic sources (speakers reproducing synthesized or recorded sounds)
- Industrial sounds (machinery, motors, traffic)

**Where Does It Vibrate?**

- In what kind of space? (affects acoustic reflections)
- How close to walls/floor/ceiling? (affects frequency buildup)
- Indoors or outdoors? (presence or absence of reverb)

**Context Matters:**

- A violin in a concert hall vs. a practice room vs. a parking garage = three completely different sounds, even with the same player and instrument
- Your voice in a closet vs. a bathroom vs. outside

# Variable #2: Transduction (The Microphone) - Full Explanation
### The First Big Shift: Microphones

_Alright, this is the first major transformation: taking physical vibrations in air and turning them into electrical voltage. This process is called TRANSDUCTION."_

**The Fundamental Concept:**

_"A microphone is basically a reverse speaker. In a speaker, you put in electrical signal and get physical vibration. In a microphone, you put in physical vibration and get electrical signal._

_At the heart of every microphone is a DIAPHRAGM—a thin membrane that vibrates when sound waves hit it. That vibration then needs to be converted into an electrical signal, and there are different ways to do that, which gives us different types of microphones."_



### Mic Types 

**Dynamic Mics:**

- Rugged, can handle loud sounds
- Less sensitive to detail
- Think: live concerts, rock vocals, drums
- Example: Shure SM58 (you've seen this at every show)

**Condenser Mics:**

- Sensitive, captures detail
- More fragile
- Think: studio recordings, quiet acoustic instruments
- Needs power (phantom power from your interface)

**Ribbon Mics:**

- Smooth, warm, "vintage" sound
- Very fragile, expensive
- Think: old-school recordings, taming harsh sounds

_"Each type has a CHARACTER. Using the 'wrong' mic isn't a mistake—it's an aesthetic choice."_

theres many more, lav mics,shotgun mics, etc etc, do your own research, ill try to get samples uploaded if i can.

---

### How Mics "Hear": Polar Patterns

_"Mics don't just hear—they hear from specific DIRECTIONS."_
![[Microphone-polar-patterns.jpg]]
So which one is the best?

### Beyond Normal Mics: Alternative Ways to Capture Sound

_"You don't have to use air mics. You can transduce (convert) other things into sound:"_

**Contact Mics:**

- Pick up vibrations through solid objects (not air)
- Stick one to a table and tap it—you hear the table's internal resonance
- Creates alien, intimate textures

**Hydrophones:**

- Underwater microphones
- Whole different sonic world

**Electromagnetic Pickups:**

- How electric guitars work
- Can pick up electrical interference (phones, power lines)
- Creates that buzzing, humming sound
**Bioelectric Signals:**

- Muscle sensors (EMG sensors picking up electrical signals from muscles)
- Heartbeat sensors
- Brain waves (EEG sonification—turning brain activity into sound)

_"You can turn ANYTHING into sound: vibrations in plants, electromagnetic fields, water, ice, electrical signals. The source doesn't have to be 'acoustic' sound."_

Multimeter, voltage, drawings, interaction on a screen, the choices are limiltess







SO NOW, we have a sound(or other input), and we have converted it to an ELECTRIC signal. How does this part of the chain works? 

Mic gives us a low signal, we need to make it louder. But how much?

### Amplification (Making It Louder)

_"Mic signals are super weak—you need to amplify them. But there are different ways to do this:"_

**Clean Amplification:**

- Transparent, no added character
- Just makes it louder

**Driven Amplification:**

- Pushes the signal harder, adds warmth/grit
- Think: guitar amps cranked up, vintage recording gear
- Adds harmonic richness

**Clipping/Distortion:**

- Too much gain = breakup, distortion
- In traditional recording: bad
- In creative contexts: texture, aggression, punk aesthetic



# The BIG Guy Analog → Digital (ADC)
_Now we convert the electrical signal into NUMBERS that a computer can work with. This is called ADC: Analog-to-Digital Conversion."_

**The Concept:** Imagine you're trying to draw a smooth curve, but you can only use dots. The more dots you use, the smoother it looks. That's what digital audio does—it takes snapshots of the sound wave

**Two settings control the 'resolution':**

Clean Sound
![[00_clean_reference.wav]]
---
Different Types of Preamping
![[01_preamp_clean.wav]]

![[02_preamp_hot.wav]]

![[03_preamp_overdriven.wav]]
#### **1. SAMPLE RATE (How Many Snapshots Per Second)**

Think of sample rate like frame rate in video. 60fps is smooth, 24fps is cinematic, 12fps is choppy/stop-motion. Same idea—different aesthetics, not better/worse


**Common rates:**

- **44.1 kHz** = CD quality (44,100 snapshots per second)
- **48 kHz** = video standard
- **22 kHz** = lo-fi but usable
- **8 kHz** = telephone quality

_"Lower sample rate = duller, darker sound (less high frequencies). But that can be an aesthetic:_

- _22 kHz = slight lo-fi warmth_
- _8 kHz = telephone/walkie-talkie vibe_
- _Can evoke specific technologies or eras"_

![[04_samplerate_48k.wav]]
![[07_samplerate_8k.wav]]
---

#### **2. BIT DEPTH (How Precisely You Measure Each Snapshot)**

**Think of it like:** _How many colors are available in a drawing?_

- High bit depth = millions of colors (smooth gradients)
- Low bit depth = only a few colors (pixelated, stepped)

**Common depths:**

- **24-bit** = professional studio standard (16 million levels)
- **16-bit** = CD quality (65,000 levels)
- **8-bit** = video game sound (256 levels) — crunchy, grainy
- **4-bit** = extremely lo-fi (16 levels) — harsh, stepped

_"Lower bit depth = grainier, crunchier texture. Think old video games—that crunchy, pixelated sound."_

---

- 48kHz/24-bit (reference - clean, full)
- 22kHz/16-bit (lo-fi - darker, slightly grainy)
- 8kHz/8-bit (telephone - very dull, crunchy)
- Extreme bit-crushing (4-bit - heavily distorted, stepped)
![[09_bitdepth_32bit 1.wav]]

![[11_bitdepth_8bit.wav]]
![[14_bitdepth_2bit_crushed.wav]]

_"Which is 'better'? Depends on what you're making. Lo-fi can be nostalgic, warm, intimate. 8-bit evokes retro gaming. Neither is wrong—they're aesthetics."_

**The Nyquist Theorem:** _"There's a fundamental rule in digital audio called the Nyquist Theorem. It says:_

_To accurately reproduce a frequency, you need to sample at TWICE that frequency._

_Humans can hear up to about 20 kHz (20,000 Hz). So to capture all audible frequencies, you need to sample at at least 40 kHz._

_That's why CD quality is 44.1 kHz—it's just above the minimum needed to capture all human hearing."_

Before we get into this, lets just talk about codecs and file compression fora. bit. 

How does a computer store sound?
How does a computers store an image?

#### **UNCOMPRESSED FORMATS (WAV, AIFF)**

**What They Are:** _"These formats store the raw sample data with minimal processing—just a header (file info) and then all the samples._

- **WAV** (Waveform Audio File Format) - Microsoft/IBM standard, most common on PC
- **AIFF** (Audio Interchange File Format) - Apple standard, common on Mac

_They're basically identical in quality—just different container formats."_

**Characteristics:**

- **Lossless** - perfect quality, no data thrown away
- **Large file sizes** - no compression, every sample stored
- **Fast to work with** - no decoding needed
- **Professional standard** - archival, studio work

**File Size Math:** _"Let's calculate:_

- _44.1 kHz sample rate_
- _16-bit depth_
- _Stereo (2 channels)_
- _1 minute of audio_

_44,100 samples/sec × 2 bytes/sample (16-bit) × 2 channels × 60 seconds = ~10 MB per minute_

_At 24-bit, it's even bigger—about 15 MB per minute._

_That adds up fast. A 40-minute album at 24-bit/48kHz stereo = about 1 GB."_


#### **LOSSLESS COMPRESSION (FLAC, ALAC)**

**What They Are:** _"These formats use compression algorithms (like ZIP for files) to reduce file size WITHOUT losing any audio data._

- **FLAC** (Free Lossless Audio Codec) - open-source, very common
- **ALAC** (Apple Lossless Audio Codec) - Apple's version, used in iTunes/Music
- **WavPack, Monkey's Audio** - less common lossless formats

_When you decompress them, you get back EXACTLY the original data—bit-for-bit identical."_

**Characteristics:**

- **Lossless** - perfect quality
- **Smaller than WAV** - typically 40-60% of original size
- **Slower to decode** - requires processing, but modern computers handle it fine
- **Archival use** - when you want to save space but keep quality
#### **LOSSY COMPRESSION (MP3, AAC, OGG)**

**What They Are:** _"These formats throw away audio data to achieve much smaller file sizes. They use 'perceptual coding'—algorithms that analyze what humans CAN'T hear and remove it."_

**How Perceptual Coding Works:** _"Human hearing has limits and quirks:_

- _We can't hear below 20 Hz or above 20 kHz_
- _We're more sensitive to some frequencies than others (midrange)_
- _Loud sounds MASK quiet sounds near them in frequency (psychoacoustic masking)_

_MP3 encoders analyze the audio and remove:_

- _Frequencies outside human hearing_
- _Quiet sounds that are masked by loud sounds_
- _Subtle details that most people won't notice_

_The result: MUCH smaller file, but you can never get the original back. The data is gone."_

**Common Formats:**

- **MP3** - most universal, older, widely supported
- **AAC** - newer, better quality at same bitrate, used by Apple/YouTube
- **Ogg Vorbis** - open-source, used in gaming/streaming
- **Opus** - newest, very efficient, used for VoIP/streaming

**Bitrate:** _"Lossy formats are defined by their BITRATE—how many kilobits per second (kbps) they use._

- **320 kbps** - highest MP3 quality, close to transparent (hard to tell from original)
- **192 kbps** - good quality, most people can't tell the difference
- **128 kbps** - decent, but artifacts become noticeable (loss of highs, "swirly" artifacts)
- **64 kbps** - low quality, obvious artifacts, but small files
- **32 kbps** - very low quality, heavy artifacts, but tiny files (used for voice, old streaming)

An mp3 at 320k
![[16_compression_mp3_320k 1.mp3]]
An Mp3 at 32k
![[19_compression_mp3_32k.mp3]]

_Higher bitrate = better quality but larger file."_



**WAV/AIFF:**

- Uncompressed, perfect quality
- Huge file sizes
- Professional standard

**MP3/AAC:**

- Compressed, smaller files
- Throws away "inaudible" information
- Creates artifacts (swirly, watery textures in cymbals/highs)

**Low bitrate MP3:**

- Very aggressive compression
- Obvious quality loss
- But: might be exactly the aesthetic you want (lo-fi bedroom pop)

### Generation Loss: The Sound of Decay

_"Every time you convert to MP3, you lose data. If you convert AGAIN, you lose more. This compounds."_


![[21_generation_loss_3x.mp3]]

![[22_generation_loss_5x.mp3]]

![[23_generation_loss_10x.mp3]]
# Digital Domain (Where Anything Is Possible)
This is where you have done most of your stuff so far.
Once sound is digital—just numbers in a computer—you can do ANYTHING. There are no physical limits anymore


_Digital audio is just data—numbers in a spreadsheet, essentially. And you can manipulate those numbers in infinite ways:_

- _Mathematical operations (add, multiply, invert)_
- _Algorithms (filters, effects)_
- _Transformations (frequency domain, spectral processing)_
- _Destruction (deliberate corruption)_

_There are NO physical limitations anymore. In the analog world, you're constrained by physics—circuits, tape, mechanics. In the digital world, the only limit is processing power and imagination_

#### **1. FILTERS & EQ (Changing Frequency Balance)**

**What It Does:** _"Filters and EQ change the frequency balance—boost or cut specific frequency ranges."_

**Types of Filters:**

**High-Pass Filter (HPF):**

- Removes low frequencies, lets highs pass through
- Use: remove rumble, thin out muddy sounds
- Extreme use: remove almost everything, leave only brittle highs

**Low-Pass Filter (LPF):**

- Removes high frequencies, lets lows pass through
- Use: remove harshness, create darkness/distance
- Extreme use: telephone/underwater effect

**Band-Pass Filter:**

- Only allows a specific frequency range through
- Use: isolate midrange, create "telephone" or "radio" effects
- Extreme use: super narrow (almost resonant, whistling)
**Creative extremes:**

- Cut all the midrange → sounds hollow, like it's in another room
- Boost a single frequency massively → creates harsh resonance
- Classic "telephone filter" → only midrange, no bass or treble


Types of EQ
![[27_eq_bass_boost.wav]]

![[28_eq_treble_boost.wav]]

![[29_eq_scooped_mids.wav]]

![[30_eq_telephone_bandpass.wav]]

#### **2. REVERB & DELAY (Creating Spacetime)**

**Reverb = simulating (or inventing) acoustic spaces**

- Small room reverb = intimacy
- Huge hall reverb = grandeur
- Extreme reverb (10+ second decay) = washes everything into ambient texture

![[31_reverb_short.wav]]

![[32_reverb_hall.wav]]

![[33_reverb_cathedral.wav]]

**Delay = repetitions**

- Short delays = thickening
- Long delays = distinct echoes
- Feedback extremes = runaway echo that builds
![[34_delay_pingpong.wav]]
#### **3. DISTORTION & EFFECTS**(Modulation)
**What They Do:** _"These effects modulate (change over time) some parameter of the sound, usually using an LFO (Low-Frequency Oscillator)."_

**Chorus:**

- Creates multiple slightly detuned copies of the sound
- Makes one instrument sound like multiple instruments
- Use: thicken guitars, synths, vocals
- Extreme: heavy detuning sounds wobbly, seasick

![[35_chorus.wav]]
**Flanger:**

- Short delay with feedback, modulated delay time
- Creates sweeping, jet-plane whoosh sound
- Use: psychedelic texture, movement
- Extreme: harsh, metallic, aggressive

![[36_flanger.wav]]

**Phaser:**

- Creates notches in the frequency spectrum that sweep over time
- Sounds like swirling, sweeping filter
- Use: subtle movement, psychedelic texture
- Extreme: pronounced swooshing, sci-fi

**Ring Modulation:**

- Multiplies two signals together, creating inharmonic sum and difference frequencies
- Sounds metallic, bell-like, or completely destroyed
- Use: aggressive transformation, making sounds unrecognizable
- Extreme: totally alien, Dalek voices, industrial noise


#### **DYNAMIC PROCESSING (Compression, Limiting, Expansion, Gating)**

**What They Do:** _"These effects change the volume/dynamics of the sound over time."_

**Compression:**

- Reduces the volume of loud parts, making the overall level more consistent
- Parameters: threshold (where it kicks in), ratio (how much reduction), attack/release (how fast it responds)
- Uses:
    - **Subtle**: glue a mix together, even out vocals
    - **Heavy**: pumping/breathing effect, aggressive RMS loudness
    - **Parallel**: blend compressed and uncompressed for thickness
- Extreme: squashed, lifeless, loud but dynamically flat

**Limiting:**

- Extreme compression (ratio of 10:1 or higher) to prevent peaks from exceeding a threshold
- Use: prevent clipping, maximize loudness
- Extreme: brickwall limiting causes distortion, pumping (loudness war casualties)

**Expansion:**

- Makes quiet things quieter (opposite of compression)
- Use: increase dynamic range, bring down noise floor

**Gating:**

- Cuts off sound below a threshold (silence becomes total silence)
- Use: remove unwanted noise between phrases, create stuttering effects
- Creative: rhythmic gating (synced to tempo creates choppy rhythm)

#### **PITCH & TIME MANIPULATION**

### The Philosophy of Digital Processing

_"Here's the key insight: processing isn't just about fixing problems or adding polish. It's about TRANSFORMATION._

_In the analog world, you're limited by physics. You can overdrive an amp, you can add spring reverb, you can use tape saturation—but you're still bound by physical components._

_In the digital world, you can:_

- _Stretch time without changing pitch_
- _Reverse reverb_
- _Freeze a moment and explore its texture_
- _Shift frequencies in impossible ways_
- _Create spaces that don't exist_

_This is where 'destruction as creation' happens. You can take a recording and process it so heavily that it becomes unrecognizable—but it's TRANSFORMED, not just destroyed. It's a new thing."_

![[37_pitch_down_octave.wav]]

![[38_pitch_up_octave.wav]]

![[39_pitch_demonic.wav]]

![[40_time_half_speed.wav]]

![[41_time_double_speed.wav]]

![[42_time_extreme_stretch.wav]]
### Feedback Loops

_"Amplification + microphones = potential for feedback. And while feedback is usually avoided (it's LOUD and can damage speakers), it can also be an instrument._

**Feedback as Texture:**

- Low-level feedback (gentle ringing)
- High-level feedback (screaming, overwhelming)
- Feedback through effects (delays, reverbs) creates complex interactions



### Datamoshing: Breaking the Format

_"You can intentionally corrupt files to create glitch effects:"_

- Delete random bytes from an MP3
- Change file formats incorrectly
- Simulate streaming errors

Datamosh:
codec switch

![[24_datamosh_codec_switch.wav]]

dropout
![[25_datamosh_dropout.wav]]
scrambled
![[26_datamosh_scrambled.wav]]
# Digital → Back to the Real World
### DAC: Numbers Back to Electricity
To hear sound, we convert numbers back into electrical signals (DAC: Digital-to-Analog Conversion). This happens in:

- _Your laptop/phone_
- _Audio interface_
- _Bluetooth speakers_
- _Anywhere digital becomes analog again_

_It's doing the opposite of ADC:_

- _ADC: continuous wave → discrete samples_
- _DAC: discrete samples → continuous wave_


**Wrong Playback Rates:** _"Here's a fun trick: if you record at one sample rate but tell the playback system it's a different sample rate, you get pitch/time shifting._

_Example:_

- _Record at 48 kHz_
- _Change the file header to say 22 kHz (or just import into a 22 kHz project)_
- _Playback reads the samples but plays them at the wrong rate_
- _Result: everything is slowed down and pitched down_

_This creates aliasing, weird harmonic content, and time distortion. It's like playing a 45 RPM record at 33 RPM."_

![[45_dac_wrong_rate_half.wav]]

![[47_dac_aliasing.wav]]

![[48_amp_fuzz.wav]]

![[49_amp_tube_saturation.wav]]

Maximum Fuckery
![[56_full_destruction.mp3]]

### Speakers: The Final Transformation

_"Different speakers sound different:"_

- Studio monitors = accurate, flat
- Phone speakers = thin, midrange-heavy
- Bluetooth speakers = bass-boosted
- **Contact transducers on objects** = object becomes the speaker

### The Room: The Invisible Instrument

_"The acoustic space shapes the sound:"_

### How Rooms Affect Sound

**Reflections:**

- Sound bounces off walls, floor, ceiling
- Creates early reflections (first few bounces) and reverberation (diffuse tail)
- Changes the frequency response (standing waves, modes, nulls)

**Room Modes:**

- Certain frequencies resonate based on room dimensions
- Can cause massive bass buildup or cancellation
- Different in every room
### Types of Spaces

**Dead Spaces (Absorptive):**

- Lots of soft materials (carpet, curtains, foam, clothes)
- Very little reverb
- Dry, intimate, close sound
- Example: bedroom closet, recording booth

**Live Spaces (Reflective):**

- Hard surfaces (tile, concrete, glass)
- Lots of reverb
- Spacious, distant, roomy sound
- Example: bathroom, stairwell, parking garage

**Outdoor (No Reflections):**

- Sound dissipates into open space
- No reverb (except distant ground reflections)
- Very dry, but in a different way than a dead room
- Can sound disconnected, lonely

**Re-amping technique:** _"Record dry, then play it through a speaker in different spaces and re-record. Capture the room itself as part of the sound."_

# **You Don't Have to Go Digital**

_"Everything we've talked about assumes digital recording. But you're not limited to that:"_

- Pure analog (tape, vinyl)
- Cassette recorders (no computer needed)
- Mechanical recording (wax cylinders, phonographs)
- Whatever weird idea you have
- Literal Mechanical Installations


# Wrap Up
_Now you know the entire chain. You understand:_

- _Where sound comes from (vibration)_
- _How it gets captured (transduction, mic choice)_
- _How it gets amplified (clean vs. colored preamps)_
- _How it gets digitized (ADC, sample rate, bit depth)_
- _How it gets stored (formats, compression, corruption)_
- _How it gets transformed (digital processing, effects)_
- _How it gets played back (DAC, speakers, space)_

_Every single arrow in that chain—every transformation—you can grab it and twist it._

_You can:_

- _Record with the 'wrong' mic_
- _Drive the preamp into distortion_
- _Use a lo-fi sample rate/bit depth_
- _Corrupt the file_
- _Process it to oblivion_
- _Play it back through a weird speaker_
- _Capture it in a strange space_

_These aren't mistakes. They're CHOICES_

Play around, have some fun.

---

**3. Choose intentionally** _"Match technique to concept:_

- _Clean = professional, modern_
- _Lo-fi = nostalgia, intimacy, DIY_
- _Distorted = aggression, punk_
- _Glitchy = digital decay, experimental_
- _Ambient = space, texture_

_The tool serves the concept."_

---

### Clean ≠ Better

_"Let's be explicit:_

**Technical perfection is ONE aesthetic, not the ONLY aesthetic.**

_Beloved sounds that embrace 'imperfection':_

- _Vinyl crackle = warmth, nostalgia_
- _8-bit sound = retro gaming_
- _Phone recordings = intimacy (bedroom pop)_
- _Cassette hiss = 80s/90s nostalgia_
- _Datamoshing = digital decay (vaporwave)_

_Each carries MEANING beyond just the sound—they communicate context, medium, era._

_When you choose lo-fi, you're not accepting poor quality—you're evoking specific associations."_




# Examples and Demo Recordings

Some more examples

Damage

![[25_damaged_cd_skip.wav]]

![[26_damaged_worn_tape.wav]]

![[27_damaged_warped_vinyl.wav]]
Distance

![[29_distance_very_close.wav]]

![[30_distance_close.wav]]

![[31_distance_medium.wav]]

![[32_distance_far.wav]]

![[33_distance_very_far.wav]]
Funky

![[44_creative_pneumatic.wav]]

![[45_creative_drone.wav]]

![[46_creative_hostile.wav]]
# Wrap up and closing ideas
this can be extensible, interactive, coded, physical, whatever you want. the DAW is merely a starting point, not the entire system

[[desc of soundscapes]]


The DAW is a starting point, not the whole system. Your sound projects can be:

- **Interactive:** sensors, movement, audience participation
- **Physical:** installations, mechanical sound-makers, objects as speakers
- **Coded:** algorithmic composition, generative systems, live processing
- **Hybrid:** any combination of the above

If you want to explore any of this—coding, electronics, installation—come talk to me. I'd love to help