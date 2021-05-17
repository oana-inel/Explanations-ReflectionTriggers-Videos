# Explanations to Support Reflective Assessment of Videos on Controversial Topics

This repository contains:
 * 960 [videos](https://github.com/oana-inel/Explanations-ReflectionTriggers-Videos/blob/main/data/video_dataset_all_topics.csv) on three controversial topics, such as "Vaccination", "Free Trade", and "Catalonia Independence", which are machine annotated with key concepts extracted from video subtitles, their sentiment (negative, neutral, positive) and emotions (fear, joy, sadness, disgust, anger);
 * 137,951 [user comments](https://github.com/oana-inel/Explanations-ReflectionTriggers-Videos/blob/main/data/video_comments) on the 960 videos, which are machine annotated with key concepts extracted from video subtitles, their sentiment (negative, neutral, positive) and emotions (fear, joy, sadness, disgust, anger);
 * 960 [explanations based on reflection triggers](https://github.com/oana-inel/Explanations-ReflectionTriggers-Videos/blob/main/data/reflection_triggers_video_dataset.csv) (one explanation per video)
 * user-centered evaluation of the effectiveness and quality of the generated explanations to support reflective assessments of socially-driven online content; ([AMT study](https://github.com/oana-inel/Explanations-ReflectionTriggers-Videos/blob/main/user_study/) with 9 videos)


## User Study

To investigate the influence of reflective triggers in natural language explanations on human assessment of online videos on controversial topics, we ran a between-subjects user study. The results of the user study are located in the [user study](https://github.com/oana-inel/Explanations-ReflectionTriggers-Videos/blob/main/user_study/) folder. The analysis of the results is located in the [notebooks](https://github.com/oana-inel/Explanations-ReflectionTriggers-Videos/blob/main/notebooks/Analysis%20of%20the%20Between-Subjects%20Study.ipynb) folder.

## Files structure

    .
    ├── data                                       # Folder storing all experimental data
    |   ├── video_dataset_all_topics.csv           # CSV containing the experimental videos and their metadata
    |   ├── video_channels_metadata.csv            # CSV containing the experimental videos channels and their metadata
    |   ├── controversial_wikipedia_pages.csv      # CSV containing the topics that are considered controversial, based on Wikipedia history 
    |   ├── reflection_triggers_video_dataset.csv  # CSV containing the reflection triggers extracted for all videos in our dataset
    |   ├── video_subtitles                        # Folder containing all video subtitles (one file per video); extracted using Google Video Intelligence API
    |   ├── video_subtitles_entities               # Folder containing all entities extracted from video subtitles (one file per video); 
    |   |                                            extracted through named entity extraction with IBM Watson Natural Language Understanding API;
    |   ├── video_subtitles_entities_topics        # Folder containing all entities extracted from video subtitles; (one file per topic); 
    |   ├── video_comments                         # Folder containing the analysis of the user comments on the videos in our dataset  
    |   |   ├── comments_sentiments_emotions.csv   # CSV containing the analysis of the comments in terms of sentiment and emotion
    │   |   ├── comments_entities.csv              # CSV containing the analysis of the comments in terms of entity extraction, and their sentiments and emotions                      
    ├── notebooks                                  # Jupyter Notebooks used for data processing
    │   ├── Generate Reflection Triggers and Explanations.ipynb   # Jupyter Notebook for entifying the reflection triggers and generating the explanations 
    │   ├── Analysis of the Between-Subjects Study.ipynb          # Jupyter Notebook used for processing the results of user study
    ├── user_study                           # Template, data and analysis of user study 1
    │   ├── user_study1_template.html         # User study 1 template (to be run on mTurk)
    │   ├── user_study1_template.md           # Visual interface of user study 1 template
    |   ├── img                               # Folder containing parts of the visual interface of user study 1
    │   ├── input_user_study1.csv             # Input file for user study 1
    │   ├── crowd_results_userstudy1.csv      # Crowdsourcing results of user study 1
    |   └── Analyze ... Study1.ipynb          # Jupyter Notebook used for processing the results of user study 1
    └──.
