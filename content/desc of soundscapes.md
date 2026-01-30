# Audio Processing Reference Guide


---

# COMPREHENSIVE SAMPLES (Script 1)

## PREAMP/GAIN STAGING (01-03)

**01_preamp_clean.wav** Clean reference signal with unity gain (1.0x). No coloration or distortion. This is your baseline - how the signal sounds when amplified just enough to reach proper level without any character added.

**02_preamp_hot.wav** "Hot" preamp gain (3.0x volume boost). Signal is pushed harder but still within headroom - not clipping yet, but getting closer to the edge. This adds a sense of presence and energy without obvious distortion. Similar to pushing an analog preamp into its sweet spot.

**03_preamp_overdriven.wav** Overdriven preamp with soft clipping (5.0x volume + limiter at 0.8). Signal is pushed well past unity, creating saturation and compression. The limiter catches the peaks and rounds them off, creating harmonic distortion. Think of a tube amp being driven hard - adds warmth and aggression.

---

## SAMPLE RATE VARIATIONS (04-08)

**04_samplerate_48k.wav** 48kHz sample rate - high quality reference. 48,000 snapshots of the waveform per second. Standard for video production, broadcast, and professional audio. Captures frequencies up to 24kHz (above human hearing range of 20kHz).

**05_samplerate_44k.wav** 44.1kHz sample rate - CD quality. 44,100 samples per second. The standard for music distribution since the 1980s. Captures up to 22.05kHz. Imperceptibly different from 48kHz for most listeners.

**06_samplerate_22k.wav** 22.05kHz sample rate - half of CD quality. Only captures frequencies up to 11kHz. Noticeably duller sound, missing high-frequency "air" and sparkle. Similar to AM radio quality. Still intelligible but clearly lo-fi.

**07_samplerate_8k.wav** 8kHz sample rate - telephone quality. Only 8,000 samples per second, capturing up to 4kHz. Very narrow bandwidth, missing both deep bass and high treble. Sounds tinny and distant but perfectly adequate for voice communication.

**08_samplerate_11k.wav** 11.025kHz sample rate - AM radio quality. Quarter of CD rate. Captures up to 5.5kHz. Sits between telephone and lo-fi music quality. Used historically for low-bandwidth audio streaming and game audio.

---

## BIT DEPTH VARIATIONS (09-14)

**09_bitdepth_32bit.wav** 32-bit sample format - extremely high resolution. Over 4 billion possible amplitude levels. More dynamic range than any recording situation requires. Used in professional digital audio workstations for processing headroom, not for final delivery.

**10_bitdepth_16bit.wav** 16-bit - CD quality. 65,536 possible amplitude levels. 96dB dynamic range (difference between quietest and loudest sounds). This is the standard for final audio delivery - transparent to human hearing when properly dithered.

**11_bitdepth_8bit.wav** 8-bit - 256 possible amplitude levels. Only 48dB dynamic range. Creates audible quantization noise (sounds like a grainy hiss). Characteristic of vintage samplers, early video games, and lo-fi aesthetics. Still intelligible but clearly degraded.

**12_bitdepth_6bit_crushed.wav** 6-bit crushing - 64 amplitude levels. Heavy digital distortion and quantization noise. The waveform's smooth curves become stepped and harsh. Creates aggressive, crunchy texture. Common in glitch music and experimental electronic production.

**13_bitdepth_4bit_crushed.wav** 4-bit crushing - only 16 amplitude levels. Extreme stairstepping of the waveform. The quantization noise is loud and harsh, almost overwhelming the original signal. Very aggressive digital distortion character.

**14_bitdepth_2bit_crushed.wav** 2-bit crushing - only 4 amplitude levels. The audio is almost completely destroyed, reduced to harsh square-wave-like pulses. Original tonal content barely recognizable. Purely in the realm of extreme sonic destruction.

---

## COMPRESSION ARTIFACTS (15-20)

**15_compression_uncompressed.wav** Uncompressed WAV reference. Every sample stored as-is with no data reduction. Large file size but perfect quality. This is your baseline for comparison with lossy formats.

**16_compression_mp3_320k.mp3** High quality MP3 at 320kbps (kilobits per second). Near-transparent to most listeners. Uses perceptual coding to remove "inaudible" frequencies but keeps most information. About 1/4 the file size of WAV.

**17_compression_mp3_128k.mp3** Standard quality MP3 at 128kbps. Acceptable for casual listening but artifacts become noticeable on critical listening: slightly blurred transients, some high-frequency "swirl," reduced stereo imaging. About 1/10 the size of WAV.

**18_compression_mp3_64k.mp3** Low quality MP3 at 64kbps. Obvious artifacts: metallic high frequencies, underwater-like modulation, loss of detail. Still intelligible but clearly degraded. Common for voice podcasts where file size matters more than quality.

**19_compression_mp3_32k.mp3** Very low quality MP3 at 32kbps. Extreme artifacts: severe high-frequency distortion, "warbling" effects, loss of stereo information. Sounds distant and processed. Only acceptable for voice in very low-bandwidth situations.

**20_compression_aac_64k.m4a** AAC compression at 64kbps. Different codec than MP3, different artifact signature. Generally sounds cleaner than MP3 at same bitrate but with its own character: slightly different frequency response, different transient handling. Used by Apple, YouTube, etc.

---

## GENERATION LOSS (21-23)

**21_generation_loss_3x.mp3** Three generations of MP3 encoding (original → MP3 → MP3 → MP3). Each encoding/decoding cycle compounds artifacts. Subtle but measurable degradation: slight high-frequency dulling, minor loss of transient detail.

**22_generation_loss_5x.mp3** Five generations of MP3 re-encoding. More noticeable artifact accumulation: frequency response shifts, compression artifacts becoming more prominent, slight "digital haze" over the sound. Historical problem in audio production workflows.

**23_generation_loss_10x.mp3** Ten generations of MP3 re-encoding. Significant degradation: obvious frequency response changes, compression artifacts clearly audible, loss of fine detail and ambience. Demonstrates why audio should stay uncompressed during production.

---

## DATAMOSHING/CORRUPTION (24-26)

**24_datamosh_codec_switch.wav** Abrupt switch from 48kHz to 8kHz mid-file without proper conversion. Creates glitchy artifact at the transition point: brief digital noise burst, sudden change in frequency content. The format itself becomes audible as it fails.

**25_datamosh_dropout.wav** Simulated buffer underrun - section of audio data replaced with silence. Creates unexpected dropout mid-phrase, like a skipping CD or dropped network packets. The discontinuity creates a jarring glitch effect.

**26_datamosh_scrambled.wav** Raw PCM data split into chunks and rearranged out of order. Audio plays in wrong sequence, jumping between moments. Creates stuttering, nonlinear time effect. The underlying data structure becomes the composition.

---

## EQ PROCESSING (27-30)

**27_eq_bass_boost.wav** Extreme low-frequency boost (+15dB at 100Hz). Emphasizes rumble, warmth, and body. Can sound powerful and full, or muddy and overwhelming depending on source material. Common in club/EDM production.

**28_eq_treble_boost.wav** Extreme high-frequency boost (+15dB at 8kHz). Emphasizes air, presence, and brilliance. Can sound crisp and detailed, or harsh and sibilant. Useful for adding clarity or creating aggressive character.

**29_eq_scooped_mids.wav** "Scooped" EQ curve: mids cut (-20dB at 500Hz), lows and highs boosted (+10dB at 100Hz and 8kHz). Classic metal guitar tone, also used in EDM. Creates "smile curve" on EQ display. Sounds powerful but can lack body and intelligibility.

**30_eq_telephone_bandpass.wav** Narrow bandpass filter (300Hz-3kHz only). Removes both bass and treble, leaving only midrange. Characteristic telephone/radio voice quality. Thin and nasal but highly intelligible. The bandwidth of traditional telephone systems.

---

## TIME-BASED EFFECTS (31-36)

**31_reverb_short.wav** Short room reverb (100ms decay). Adds subtle sense of space without overwhelming the dry signal. Sounds like a small room or booth. Quick reflections give presence without muddiness.

**32_reverb_hall.wav** Large hall reverb (300-600ms decay). Medium-to-long reverb tail creates sense of performing in a concert hall. Adds majesty and depth. Multiple echo parameters create dense, smooth reverb character.

**33_reverb_cathedral.wav** Cathedral reverb (500-1500ms decay). Very long reverb tail with high-frequency roll-off creating dark, spacious character. Extremely long decay creates wash of sound. Evokes massive stone architecture.

**34_delay_pingpong.wav** Ping-pong delay effect (500ms with 60% feedback). Creates rhythmic echo that bounces in stereo field. Single delay tap with moderate feedback creates repeating echoes that gradually fade.

**35_chorus.wav** Chorus effect - creates multiple slightly detuned copies of the signal. Adds width, shimmer, and movement. Simulates multiple performers or creates synthetic "analog" warmth. Classic 1980s production sound.

**36_flanger.wav** Flanger effect - short delay with feedback and LFO modulation. Creates sweeping, jet-plane-like whoosh. Metallic, swirling character. Extreme version of chorus with more pronounced modulation.

---

## PITCH/TIME MANIPULATION (37-42)

**37_pitch_down_octave.wav** Pitched down one octave (halved playback speed, then resampled). Everything sounds exactly one octave lower while maintaining original duration. Creates deeper, darker version of source.

**38_pitch_up_octave.wav** Pitched up one octave (doubled playback speed, then resampled). Everything sounds exactly one octave higher. Creates chipmunk/helium effect. Brighter, faster feeling.

**39_pitch_demonic.wav** Pitch shifted down 20% (0.8x playback rate). Not a full octave - creates unnatural, slowed character without being obviously "pitched down." Subtle but disturbing shift. Classic "demon voice" processing.

**40_time_half_speed.wav** Time-stretched to half speed using atempo filter. Maintains original pitch while doubling duration. Everything sounds slower and more drawn out but at correct frequency. Reveals detail in fast passages.

**41_time_double_speed.wav** Time-stretched to double speed using atempo filter. Maintains original pitch while halving duration. Creates rushed, urgent feeling without pitch change. Compresses time while preserving tonal content.

**42_time_extreme_stretch.wav** Extreme time stretch (1/8 speed, three atempo passes at 0.5x each). Drastically slowed without pitch change. Creates dreamy, suspended quality. Can reveal micro-details or create ambient textures from transients.

---

## DAC/WRONG PLAYBACK (43-47)

**43_dac_48k_as_44k.wav** Audio recorded at 48kHz, played back as if it were 44.1kHz. Plays slightly slower and lower in pitch (about 8.8% slower). Subtle but noticeable shift. Historical problem when mixing sample rates.

**44_dac_44k_as_48k.wav** Audio recorded at 44.1kHz, played back as if it were 48kHz. Plays slightly faster and higher in pitch (about 8.8% faster). Creates rushed, slightly chipmunk-like quality.

**45_dac_wrong_rate_half.wav** Audio played back at half the intended sample rate. Sounds exactly one octave lower and twice as long. Extreme version of wrong playback rate - completely different character.

**46_dac_wrong_rate_double.wav** Audio played back at double the intended sample rate, creating aliasing artifacts. Sounds one octave higher but with digital artifacts from improper resampling. The "foldover" frequencies create harsh, metallic quality.

**47_dac_aliasing.wav** Extreme aliasing from severe sample rate mismatch (8kHz resampled to 44.1kHz). High frequencies that exceeded the Nyquist limit "fold back" into audible range, creating inharmonic, metallic artifacts. The math of digital audio becomes audible.

---

## AMPLIFICATION DISTORTION (48-50)

**48_amp_fuzz.wav** Fuzz distortion (10x volume + hard limiter at 0.3). Extreme clipping creates square-wave-like waveform. Harsh, aggressive, sustained distortion. Think vintage fuzz pedal - completely transforms signal into thick, saturated wall.

**49_amp_tube_saturation.wav** Soft tube-style saturation (2.5x volume + compander). Gentle, musical distortion with compression. Rounds off peaks smoothly rather than hard clipping. Adds warmth and harmonic richness without harshness.

**50_amp_hard_clip.wav** Hard digital clipping (8x volume + limiter at 0.5). Severe clipping with fast attack/release. Creates harsh, square-topped waveform. More aggressive than tube saturation - bright, cutting distortion.

---

## COMBINED/EXTREME EFFECTS (51-56)

**51_combined_lofi.wav** Lo-fi aesthetic: 8-bit crushing + gentle bandpass (100Hz-8kHz) + slight volume reduction + 96kbps MP3 compression. Creates warm, nostalgic, vintage digital sound. Characteristic of lo-fi hip-hop, bedroom pop, cassette simulation.

**52_combined_telephone.wav** Telephone simulation: narrow bandpass (300Hz-3.4kHz) + 8-bit crushing + 8kHz sample rate + 32kbps compression. Recreates limited bandwidth of phone system. Thin, nasal, distant but intelligible.

**53_combined_underwater.wav** Underwater effect: severe lowpass (800Hz cutoff) + medium reverb + chorus. Muffled, pressure-like quality. Sound seems to move slowly through dense medium. Dreamy, submerged character.

**54_combined_robot.wav** Robot voice: pitch down 15% + 6-bit crushing + vibrato modulation. Creates mechanical, synthesized character. Slightly inhuman but still intelligible. Classic sci-fi robot vocalization.

**55_combined_destroyed.wav** Extreme destruction: 4-bit crushing + pitch down 30% + echo + overdrive/clipping + 48kbps compression. Multiple degradation layers compound. Nearly unrecognizable transformation of source. Pure texture over content.

**56_full_destruction.wav** Complete signal chain abuse: 6-bit crushing + overdrive + bandpass + reverb + pitch down 20% + downsample to 22kHz + 64kbps compression. Every stage adds degradation. The sum of all possible "wrong" choices.

---

# SOUNDSCAPES SAMPLES (Script 2)

## SPECTRAL PROCESSING (01-05)

**01_spectral_extreme_paulstretch.wav** Extreme time-stretching using sample rate manipulation + multiple atempo passes. Audio stretched to 10x duration or more. Individual grains of sound become elongated drones. Transients smear into sustained tones. Similar to Paul's Extreme Sound Stretch algorithm.

**02_spectral_reverse.wav** Audio played backwards (areverse filter). Time-reversed: attacks become releases, releases become attacks. Reveals the "backwards" character of sound - sucks inward rather than projects outward. Creates unnatural, dreamlike quality.

**03_spectral_reverse_reverb.wav** Reverb applied, then reversed. Creates "reverse reverb" or "preverb" effect - sound builds up before the hit. The tail leads instead of follows. Classic psychedelic/experimental production technique.

**04_spectral_granular_sim.wav** Granular-like texture created with time stretch + short echo. Audio broken into small grains that overlap. Creates stuttering, textural quality. Not true granular synthesis but similar aesthetic using delay-based approach.

**05_spectral_freq_shift.wav** Frequency shifting simulation using vibrato. All frequencies shifted by same amount (not pitch shift which maintains harmonic relationships). Creates inharmonic, metallic quality. Vibrato at 5Hz with deep modulation approximates frequency shifter.

---

## SPATIAL/ROOM SIMULATIONS (06-11)

**06_space_closet_dead.wav** Dead acoustic space (closet with clothes): severe highpass/lowpass creating narrow bandwidth (200Hz-4kHz) + volume reduction. Sounds muffled and intimate. No reflections or reverb. Characteristic of heavily damped spaces.

**07_space_bathroom.wav** Bathroom tiles acoustics: short, bright reverb (50-100ms) + high-frequency boost at 3kHz. Hard, reflective surfaces create slap echo. Bright, live character. Small room with tile creates quick, harsh reflections.

**08_space_stairwell.wav** Stairwell acoustics: multiple reverb layers (200ms, 400ms, 800ms) creating flutter echo effect. Parallel walls create rhythmic reflections. Long, ringing character. Sound bounces up and down the vertical shaft.

**09_space_parking_garage.wav** Parking garage: long reverb with metallic emphasis (boost at 1kHz). Concrete and metal surfaces create harsh, industrial reverb. Cold, inhospitable character. Large space but not pleasant-sounding reverb.

**10_space_open_field.wav** Outdoor/field recording: minimal processing - just gentle highpass/lowpass + slight volume boost. No reverb or reflections. Sound disappears into space. Clear and direct but lacks body that rooms provide.

**11_space_cathedral.wav** Cathedral acoustics: very long reverb (500-1500ms) with high-frequency roll-off creating dark, smooth tail. Stone architecture creates long, majestic decay. Lows sustained, highs absorbed. Sense of massive volume.

---

## TRANSMISSION MEDIUM SIMULATIONS (12-18)

**12_medium_am_radio.wav** AM radio: limited bandwidth (300Hz-5kHz) + bit crushing for noise floor + downsampled to 22kHz. Narrow frequency range with some noise. Intelligible but clearly mediated. Characteristic tinny AM broadcast sound.

**13_medium_fm_radio.wav** FM radio: cleaner than AM but still bandwidth-limited (50Hz-15kHz) + downsampled to 32kHz. More natural than AM but still not full fidelity. Slight high-end roll-off. Standard broadcast FM quality.

**14_medium_shortwave.wav** Shortwave radio: very narrow bandwidth (400Hz-4kHz) + heavy bit crushing + vibrato for interference. Noisy, unstable signal. Characteristic of long-distance radio transmission. Lots of static and modulation.

**15_medium_walkie_talkie.wav** Walkie-talkie: narrow bandwidth (500Hz-3kHz) + 8-bit crushing + 8kHz sample rate + compression/limiting. Characteristic squashed, lo-fi two-way radio sound. Aggressive limiting for transmission efficiency.

**16_medium_intercom.wav** PA system/intercom: moderate bandwidth (300Hz-6kHz) + volume boost + limiting + midrange emphasis at 1kHz. Slightly overdriven, compressed sound. Optimized for speech intelligibility over quality.

**17_medium_underwater.wav** Underwater transmission: severe lowpass (600Hz cutoff) + reverb + volume reduction. Only low frequencies transmit through water. Muffled, pressure-like quality. Sound moves slowly, high frequencies absorbed.

**18_medium_through_wall.wav** Through wall/door: strong lowpass (1.2kHz cutoff) + bass boost at 200Hz + volume reduction. High frequencies blocked by mass, low frequencies pass through. Muffled but bass-heavy. Can feel vibrations more than hear detail.

---

## VINTAGE/ANALOG MEDIA (19-24)

**19_vintage_vinyl.wav** Vinyl record: gentle highpass (30Hz) and lowpass (14kHz) + slight bass boost at 100Hz + mild bit crushing (14-bit) for surface noise simulation + volume reduction. Warm, slightly rolled-off character. Subtle "analog" quality.

**20_vintage_cassette.wav** Cassette tape: highpass at 12kHz + slow vibrato (0.2Hz) for tape warble + moderate bit crushing (12-bit) for tape hiss. Characteristic wow and flutter. High-end dulled. Warm but slightly unstable.

**21_vintage_reel_to_reel.wav** Reel-to-reel tape: gentle highpass (40Hz) and lowpass (18kHz) + subtle bass boost at 150Hz. Cleanest of analog formats. Warm but extended frequency response. Professional analog sound without severe limitations.

**22_vintage_wax_cylinder.wav** Wax cylinder: extreme bandwidth limiting (500Hz-2.5kHz) + heavy bit crushing (6-bit) + volume reduction + downsampled to 11kHz. Characteristic of pre-1920s recording. Barely recognizable as original source. Mechanical, distant, ancient.

**23_vintage_phonograph.wav** Edison phonograph: even more severe than wax cylinder (600Hz-2kHz) + extreme bit crushing (5-bit) + midrange scoop + downsampled to 8kHz. Oldest recording technology. Tinny, mechanical, barely intelligible. Historical artifact sound.

**24_vintage_vhs.wav** VHS audio track: moderate lowpass (10kHz) + bit crushing (10-bit) + slow vibrato for tracking errors. Characteristic of consumer video tape. Slightly muffled and unstable. Nostalgic 1980s-90s home video sound.

---

## DAMAGED/DEGRADED MEDIA (25-28)

**25_damaged_cd_skip.wav** Scratched CD skip: PCM data manipulation - small section repeated multiple times creating stutter, then jumps forward. Characteristic digital skip - clean audio then sudden repetition and jump. The CD player's error correction fails.

**26_damaged_worn_tape.wav** Worn cassette tape: vibrato for flutter (0.5Hz) + lowpass (8kHz) + volume reduction. Tape stretching creates pitch instability. High-frequency loss from oxide wearing off. Characteristic of over-played tapes.

**27_damaged_warped_vinyl.wav** Warped vinyl: slow, deep vibrato (0.3Hz) + gentle lowpass (10kHz). Record dish-shaped from heat/storage creates cyclical pitch variation. One "wow" per rotation. Nauseating pitch drift.

**28_damaged_water.wav** Water-damaged media: random PCM dropouts (sections replaced with silence) + lowpass filter (4kHz). Water destroys random sections of magnetic media. Creates unexpected silences and muffled sound. Permanent data loss artifacts.

---

## DISTANCE/PERSPECTIVE (29-33)

**29_distance_very_close.wav** Very close mic placement: proximity effect simulation - heavy bass boost at 150Hz + highpass at 80Hz + volume boost. Characteristic of being inches from microphone. Intimate, present, bass-heavy. Can feel breath and detail.

**30_distance_close.wav** Close/natural distance: unprocessed reference. Natural balance without proximity effect or room tone. Direct sound dominates. This is the "neutral" perspective most recordings aim for.

**31_distance_medium.wav** Medium distance: subtle room tone (low-level echo at 100ms) + slight volume reduction. Mix of direct and reflected sound. Beginning to hear the space. More natural but less intimate.

**32_distance_far.wav** Far distance: lowpass (8kHz) + moderate reverb (200-400ms) + volume reduction. More reverb than direct sound. Muffled by air absorption. Sense of distance and space. Can still identify source clearly.

**33_distance_very_far.wav** Very far distance: strong lowpass (4kHz) + heavy reverb (400-1200ms) + significant volume reduction. Barely hear direct sound - mostly reflections. Highly muffled. Sound at edge of intelligibility. Approaching ambience.

---

## ENVIRONMENTAL EFFECTS (34-39)

**34_env_wind_rumble.wav** Wind buffeting microphone: extreme low-frequency emphasis - highpass at 30Hz, lowpass at 200Hz + volume boost. Simulates wind hitting microphone diaphragm. Deep rumble. Characteristic of outdoor recording without windscreen.

**35_env_rain_filter.wav** Rain ambience filtering: highpass at 1kHz + volume reduction. Simulates the frequency content of rain sound itself - mostly high-frequency noise. Gentle hiss of water droplets. The "background" of rain recordings.

**36_env_thunder.wav** Thunder/distant boom: severe lowpass (500Hz only) + long reverb (500-1000ms) + volume boost. Only low frequencies travel long distances. Rolling, rumbling character. Long decay from distance. Feels low-frequency pressure wave.

**37_env_in_car.wav** Inside car/vehicle: strong lowpass (3kHz) + highpass (100Hz) + midrange boost at 500Hz. Glass and metal create specific frequency response. Muffled exterior world. Road noise emphasis. Enclosed but not dead space.

**38_env_in_helmet.wav** Inside helmet/enclosed head space: moderate bandpass (200Hz-5kHz) + short echo (30ms) + volume boost. Sound trapped close to ears. Slight resonance. Muffled but pressurized feeling. Own breathing prominent.

**39_env_megaphone.wav** Megaphone/bullhorn: bandpass (400Hz-4kHz) + extreme volume boost + hard limiting + midrange emphasis at 1.5kHz. Designed to project speech over distance. Harsh, aggressive, attention-grabbing. Sacrifices quality for volume and intelligibility.

---

## CREATIVE/ABSTRACT PROCESSING (40-50)

**40_creative_glitch_stutter.wav** Glitch stutter: PCM data manipulation - small chunks (0.1 second) repeated 5 times before continuing. Creates rhythmic stuttering effect. Time hiccups and repeats. Characteristic of buffer errors turned into aesthetic choice.

**41_creative_metallic.wav** Metallic resonance: narrow peaks at 1kHz and 2kHz (high Q) + short echo with high feedback. Resonant frequencies ring out. Creates bell-like or metallic quality. Emphasizes inharmonic partials.

**42_creative_crystalline.wav** Crystalline/ice texture: highpass at 2kHz (removes all bass) + extreme treble boost at 8kHz + short bright reverb. Only highest frequencies remain. Delicate, glassy, fragile quality. Emphasis on transients and shimmer.

**43_creative_liquid.wav** Organic/liquid texture: chorus effect + gentle lowpass (6kHz) + slight volume reduction. Chorusing creates movement and fluidity. Slightly dulled high end. Undulating, flowing quality. Warbling modulation suggests liquid motion.

**44_creative_pneumatic.wav** Pneumatic/air pressure: bandpass at 2kHz + bit crushing (10-bit) + volume boost. Narrow frequency range emphasizes "whoosh" of air. Slight distortion. Mechanical breath. Compressed air release character.

**45_creative_drone.wav** Drone-ification: extreme time stretch (1/8 speed) + pitch down one octave + volume reduction. Fast sounds become sustained tones. Transients stretched into evolving textures. Ambient, meditative, suspended in time.

**46_creative_hostile.wav** Hostile/aggressive: harsh midrange boost at 2kHz + extreme overdrive (4x volume + limiting) + bit crushing (8-bit). Painful frequency emphasis. Heavy distortion. Unpleasant, confrontational, tense. Designed to create discomfort.

**47_creative_dreamlike.wav** Dream-like/surreal: reverb added then reversed + slight pitch down (5%). Preverb effect creates backwards quality. Slight detune adds instability. Unnatural, ethereal, suspended. Sound seems to breathe inward.

**48_creative_spectral_freeze.wav** Spectral freeze simulation: extreme echo feedback (0.99 at 1 second, 0.98 at 2 seconds) + gentle lowpass (8kHz). Echoes decay so slowly they sustain almost indefinitely. Creates "frozen" quality where sound hangs in air.

**49_creative_granular_cloud.wav** Granular cloud: time stretch + multiple short echoes with high feedback. Sound broken into overlapping grains. Dense, textural quality. Not discrete repetitions but merged cloud of micro-sounds.

**50_creative_time_folding.wav** Time-domain folding: PCM manipulation - middle third of audio reversed while beginning and end play forward. Creates palindrome-like structure. Time flows forward, then backward, then forward. Disorienting narrative disruption.

---

Each file demonstrates specific processing techniques and their sonic results. Use these as reference points for understanding how different processes affect audio, and as jumping-off points for your own explorations.