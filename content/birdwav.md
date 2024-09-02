yesterday(1 sep24) i was in conversation with my friend harsh and we were discussing this syneshetic thought he had about looking up at birds flying through the sky, and hearing it as music.

I am attempting to bring that to life, translating the birds flight patterns into sound. This is a documentation of that attempt.

I am trying to use opencv to detect the birds flight patterns and duration across frames of a video. i am using this video as a sample. https://www.youtube.com/watch?v=YCNwIrAISek

In my first few attempts, i was getting very short tones due to only producing a millisecond of sound per frame, leading to a short harsh buzz sounding like this 


![[bird_flight_synth4.wav.wav]]

I then removed the association of the duration with the y-cooridnate, and based the duration as a multiple of the video's frame rate.

then i got this
the time of audio per frame is now the same time as the video frame time

![[bird_flight_synth5.wav]]

kinda harsh and death metally eh



now i