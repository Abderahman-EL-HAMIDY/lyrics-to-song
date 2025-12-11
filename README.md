# Lyrics to song
This project presents an approach to building a generative AI system that creates complete songs from lyrics + genre.

--------------------------
### how system works
A song can be viewed as two main components:
instrumentals + vocals (the lyrics sung by a voice).

Based on this idea, we designed an architecture composed of three models:

![Model Architecture]('System%20Architecture.png')

- Melody Composer: We fine-tuned LLaMA 3-8B to generate melodies in ABC notation.
The ABC sequence is then converted into audio, and this melody is used as a conditioning signal for the other models.

- Instrumental Generation: We use MusicGen-Melody, which takes the melody (and optionally the genre or mode) as input and generates the instrumental track.

- Singing Voice Synthesis: We use the Bark model to generate the sung vocals directly from the lyrics.

