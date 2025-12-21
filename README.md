# Lyrics to song
This project presents an approach to building a generative AI system that creates complete songs from lyrics + genre.

--------------------------
### how system works
A song can be viewed as two main components:
instrumentals + vocals (the lyrics sung by a voice).

Based on this idea, we designed an architecture composed of two models:

![Model Architecture](System_Architecture.png)

- Singing Voice Synthesis: We use the Bark model to generate the sung vocals directly from the lyrics.
- Instrumental Generation: We use MusicGen-Melody, which takes the melody and the genre (description of the the instrument) as input and generates the instrumental track.
