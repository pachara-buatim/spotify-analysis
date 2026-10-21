# Spotify Analysis: Exploring the Audio Features of the Most-Streamed Songs
## Introduction

As a music producer, I've always been curious about what makes a song successful in terms of streaming.

Marketing, artist popularity, and playlist placements all play important roles in a song's success. However, I also believe that the music itself matters. A song's production, rhythm, and overall sound may influence whether listeners want to come back and listen to it again.

This curiosity inspired me to start this project. I wanted to explore the audio characteristics of the most-streamed songs on Spotify and identify patterns that might provide insights into what these tracks have in common.

## Project Objective

The main objective of this project is to explore the audio characteristics of the 100 most-streamed songs in the dataset.

Specifically, I wanted to investigate:

What tempo is most common among the most-streamed songs?
Which musical keys and modes appear most frequently?
What are the average energy, danceability, acousticness, liveness, instrumentalness, and valence levels?
Are there any interesting relationships between these audio features?
The goal is to understand the musical characteristics shared by these popular tracks, rather than to establish a definitive formula for streaming success.

## Dataset and Data Preparation

For this project, I obtained a Spotify dataset from Kaggle. The dataset was relatively clean, although some missing values were present.

To focus on the most successful tracks in terms of streaming numbers, I sorted the dataset by streams in descending order and selected the top 100 most-streamed songs.

The dataset includes several audio features:


### Feature	Description
• BPM	Tempo of a track, measured in beats per minute.
• Key	The estimated musical key of a track.
• Mode	Whether a track is in a major or minor mode.
• Energy	A measure of perceived intensity and activity.
• Danceability	How suitable a track is for dancing.
• Acousticness	An estimate of how likely a track is to be acoustic.
• Liveness	An estimate of the likelihood that a track was performed live.
• Instrumentalness	An estimate of whether a track contains no vocals.
• Valence	A measure of the musical positivity conveyed by a track.

### Data Preparation

The main preparation steps were:

1. Checked the dataset for missing values.
2. Sorted tracks by stream count in descending order.
3. Selected the top 100 most-streamed tracks.
4. Calculated average values for the numerical audio features.
5. Identified the most frequently occurring musical key and mode.
Screenshot: Data preparation and cleaning

!Data preparation

## Exploratory Data Analysis

After preparing the data, I calculated summary statistics for the audio features and examined the distribution of musical keys and modes.

## Summary of Findings

Audio Feature	Result
Average BPM	123
Most common key	C#
Most common mode	Major (64 tracks)
Average energy	65%
Average danceability	63%
Average acousticness	26%
Average liveness	17%
Average instrumentalness	0%
Average valence	51%
Note: Eleven tracks have missing key information. Instrumentalness is reported as 0%; this value should be checked against the underlying data and its rounding precision.

### Tempo

The average tempo of the top 100 tracks is 123 BPM.

This suggests that the selected tracks generally have a moderate-to-fast tempo. Such tempos are common in many pop and electronic music productions, although BPM alone cannot determine a song's genre or popularity.

Screenshot: BPM analysis

!BPM analysis

### Musical Key and Mode

C# is the most frequently occurring key among the tracks with available key data. However, 11 tracks have missing key information, which should be considered when interpreting the result.

Major mode is more common than minor mode, appearing in 64 out of the 100 tracks.

This suggests that major-mode compositions are relatively common in this group. However, a major mode does not necessarily mean a song sounds happy, just as a minor mode does not necessarily make a song sound sad.

Screenshot: Key and mode distribution

!Key and mode analysis

### Energy and Danceability

The average energy is 65%, while average danceability is 63%.

Both values suggest that the selected tracks tend to have relatively energetic and rhythmically engaging characteristics.

From a music production perspective, this is an interesting observation because energy and groove are important elements to consider when creating music intended to engage listeners.

However, these averages alone do not establish whether energy and danceability are correlated or whether either feature contributes to higher streaming numbers.

Screenshot: Energy and danceability analysis

!Energy and danceability

### Acousticness and Liveness

Average acousticness is 26%, while average liveness is 17%.

These relatively low averages suggest that the tracks tend to have lower acousticness scores and a lower estimated likelihood of being live recordings.

This may be consistent with a tendency toward studio-produced music rather than predominantly acoustic or live-performance recordings. However, these features alone cannot establish how a track was produced or recorded.

Screenshot: Acousticness and liveness analysis

!Acousticness and liveness

### Instrumentalness

The average instrumentalness is reported as 0%.

This suggests that instrumentalness scores are very low across the selected tracks. However, an average of zero does not necessarily mean that every track contains vocals, especially if values have been rounded. Instrumentalness is an estimate, not a direct vocal-presence measurement.

This result should therefore be interpreted as a characteristic of the dataset's instrumentalness scores rather than definitive proof that all 100 tracks contain vocals.

Screenshot: Instrumentalness analysis

!Instrumentalness analysis

### Valence

The average valence is 51%, which is close to the midpoint of the scale.

This suggests that the group does not have an especially high or low average valence score. However, the average alone cannot tell us how many tracks have positive or negative emotional qualities, since valence is a continuous audio feature rather than a direct classification of emotion.

Screenshot: Valence analysis

!Valence analysis

## Relationships Between Audio Features

Based on the initial analysis, I became interested in two possible relationships:

Energy and danceability: Both features have relatively high averages in the selected group.
Acousticness and liveness: Both features have relatively low averages.
These observations led me to investigate whether the features are correlated.

However, similar averages do not necessarily indicate correlation. To evaluate these relationships, correlation coefficients or a correlation heatmap would be needed.

This is an important distinction: the goal is not only to identify patterns but also to determine whether those patterns are supported by the data.

Screenshot: Audio feature correlation heatmap

!Audio feature correlation heatmap

## Key Takeaways

Based on the analysis of the top 100 most-streamed tracks, several characteristics stand out:

The average tempo is 123 BPM.
Energy and danceability have relatively high average values, at 65% and 63%, respectively.
Acousticness and liveness have relatively low average values, at 26% and 17%.
Major mode appears in 64 out of the 100 tracks.
The average valence is close to the midpoint of the scale.
Together, these results provide a descriptive overview of the audio characteristics found in the selected tracks.

From a music production perspective, these patterns are interesting starting points for exploring how musical characteristics vary among popular songs.

## Limitations

There are several limitations to consider when interpreting these findings.

The analysis focuses only on the top 100 tracks. The results describe the selected group but do not establish whether these characteristics are more common among highly streamed songs than among less-streamed songs.

Audio features cannot fully describe a song. Spotify's audio features provide useful summaries, but they do not directly measure factors such as hook memorability, vocal performance, lyrical appeal, or production quality.

Streaming success has many potential influences. Artist popularity, marketing, playlist placement, release timing, and listener preferences may also contribute to streaming performance.

Correlation does not establish causation. Even if certain audio features are correlated, that does not prove that they cause a song to receive more streams.

These limitations mean that the results should be treated as exploratory observations rather than a definitive explanation of streaming success.

## Final Dashboard

The final dashboard brings the key findings together in one place, providing an overview of the most-streamed tracks and their audio characteristics.

Screenshot: Final Spotify analysis dashboard

!Final Spotify analysis dashboard

## Conclusion

This project began with a simple question: what do the most-streamed songs on Spotify have in common?

By analyzing the top 100 most-streamed tracks in the dataset, I found that they tend to have a moderate-to-fast tempo, relatively high energy and danceability, lower acousticness and liveness, and a greater representation of major-mode tracks.

These findings offer an interesting perspective on the musical characteristics of popular songs. However, they do not establish that any particular feature makes a song successful.

Instead, this analysis provides a starting point for further exploration into the relationship between music and streaming performance.

As a music producer, I find this process valuable because it allows me to approach a familiar question from a data-driven perspective, using evidence to explore patterns rather than relying entirely on intuition.

## Tools and Technologies

Dataset: Spotify dataset from Kaggle
Data preparation and analysis: [Add your tools here]
Data visualization: [Add your tools here]
Dashboard: [Add your dashboard tool here]
This project is an exploratory analysis of the audio characteristics of the 100 most-streamed tracks in the selected dataset. Its purpose is to identify patterns and generate questions for further investigation, rather than to establish a definitive formula for streaming success.
