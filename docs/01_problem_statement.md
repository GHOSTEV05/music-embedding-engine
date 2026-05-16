# Problem Statement
## Introduction
Modern music recommendation and retrieval systems commonly rely on metadata such as genre labels, artist information, playlists, and manually assigned tags. Although these approaches are effective in many scenarios, they often fail to capture the intrinsic acoustic characteristics of audio signals, limiting the ability to identify songs that are truly similar in terms of sound, texture, rhythm, energy, or overall musical structure.

With the growth of digital music libraries and the increasing availability of audio data, there is a need for intelligent systems capable of analyzing music directly from the audio signal itself rather than depending exclusively on external metadata.

## Problem Description
Traditional metadata-based recommendation systems present several limitations:

- Songs with similar acoustic properties may belong to different genres and therefore not be identified as related.
- Manual labeling and categorization are subjective and inconsistent.
- Metadata does not fully represent the perceptual characteristics of music.
- Large music collections become difficult to organize and explore efficiently without automated similarity analysis.

As a result, users, producers, and researchers may struggle to discover acoustically similar music tracks or organize audio collections based on actual sound characteristics.

## Proposed Solution
This project proposes the development of a Machine Learning-based system capable of learning latent representations of audio signals and performing similarity search between music tracks using acoustic information extracted directly from audio files.

The system will process music files (.wav and .mp3), extract relevant audio features, and train a deep learning model capable of generating compact embeddings that represent the acoustic identity of each song.

These embeddings will then be used to compute similarity between tracks using mathematical distance metrics such as cosine similarity, enabling content-based music retrieval without relying exclusively on metadata or manual labels.

## General Objective
Design and implement a machine learning system capable of generating audio embeddings and performing music similarity search based on acoustic characteristics extracted from audio signals.

## Specific Objetives
- Analyze and preprocess audio signals from music datasets.
- Extract relevant acoustic features using digital signal processing techniques.
- Train a deep learning model to learn latent representations of music tracks.
- Generate embeddings that capture meaningful acoustic information.
- Implement similarity search using vector distance metrics.
- Design a scalable system architecture integrating backend services and machine learning components.

## Scope
The project focuses on content-based music similarity using locally available audio files and academic datasets.

The system will:

- Process .wav and .mp3 audio files.
- Generate embeddings from extracted acoustic features.
- Perform similarity search between songs.
- Provide an architecture composed of a backend service and a machine learning service.

The project will not:

- Provide music streaming functionality.
- Download copyrighted music from external platforms.
- Replace commercial recommendation systems such as Spotify.

## Expected outcome
The expected result is a functional prototype capable of identifying acoustically similar songs through learned audio representations, demonstrating the application of machine learning and representation learning techniques in the field of music information retrieval.