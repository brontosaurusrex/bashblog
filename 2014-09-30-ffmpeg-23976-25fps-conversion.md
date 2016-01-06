ffmpeg

<pre>ffmpeg -r "25" -i "in.mov" -filter:a "atempo=1.0427" "out.mov"</pre>

which is probably similar to this avisynth (only the pitch is corrected as well);

<pre>AssumeFPS(25, 1, true)                 # Convert frame rate to PAL, also adjust audio.
SSRC(48000)                            # Restore audio sample rate to a standard rate.</pre>