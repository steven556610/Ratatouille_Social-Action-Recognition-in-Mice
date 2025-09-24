# Ratatouille_Social-Action-Recognition-in-Mice

## MABe (Multi-Agent Behavior) Challenge - Social Action Recognition in Mice
> MABe Challenge - Social Action Recognition in Mice
> F score (metric) 這邊的程式碼已經寫好了
 
[kaggle](https://www.kaggle.com/competitions/MABe-mouse-behavior-detection)
[metric](https://www.kaggle.com/code/metric/mabe-f-beta)

## past literature
[MABe22 at ICML 2023](https://arxiv.org/pdf/2207.10553)
[CalMS21 at NeurIPS](https://arxiv.org/pdf/2104.0271)
[CRIM13 at CVPR] (doi: 10.1109/CVPR.2012.6247817)

## data explaination
### Files
[train/test].csv Metadata about the mice and recording setups.
* lab_id - The pseudonym of the lab that provided the data. The CalMS21, CRIM13, and MABe22 datasets are copies of publicly available datasets provided as additional training data. Some tracking files in CalMS21 set are largely duplicated-- these were annotated by multiple individuals for different sets of behaviors.
video_id - A unique identifier for the video.
* mouse[1-4] [strain/color/sex/id/age/condition] - Basic information about each mouse.
* frames per second
* video duration (sec)
* pix per cm (approx)
* video [width/height]
* arena [width/height] (cm)
* arena shape
* arena type
* body parts tracked - Each lab used different technology to track their mice, so the specific body parts tracked may vary.
* behaviors labeled - The behaviors labeled in this video. Necessary as the annotations are sparse. Each lab annotated their videos differently, may not have annotated all behaviors for a video, and may not have annotated all mice in each video.
* tracking method - The model used to track the animal's pose.
::: 
### [train/test]_tracking/ The feature data.
* video_frame
* mouse_id
* bodypart - The tracked body part. Different labs may track different body parts
* [x/y] - The body part's X/Y coordinate position in pixels.

### train_annotation/ Train labels.
* agent_id - ID of the mouse performing the behavior.
* target_id - ID of the mouse targeted by the behavior. Some behaviors, such as a mouse grooming itself, have the same agent and target ID.
* action - What behavior is occurring (e.g., grooming, chasing). Different labs annotated different behaviors.
* [start/stop]_frame - The first/last frame of the action.

### sample_submission.csv A submission file in the correct format.
* row_id - You'll need to provide a column of unique row IDs. A simple enumeration will suffice.
* video_id
* agent_id
* target_id
* action
* [start/stop]_frame



## thoughts

## literature




