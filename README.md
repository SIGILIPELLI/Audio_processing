# Audio_processing
Implementing audio processing in Python:
This will open a stream, which is a PyAudio construct that manages input and output to/from one sound device. In this case, it is configured to use float values, only open one channel, play audio at a sample rate of 44100 Hz, have that one channel be output only and call the function callback every 1024 samples. 
Since the callback will be executed on a different thread, control flow will continue immediately after pa.open(). In order to analyze the resulting signal, the while stream.is_active() loop waits until the signal has been processed completely. 
Every time the callback is called, it will have to return 1024 samples of audio data. Using the class Limiter above, a sample counter counter and an audio signal signal.
