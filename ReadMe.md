# SkillDisplay Grade Helper
A simple JavaScript snippet for calculating a school grade based on a personal set of skills.
It uses the available API for SkillDisplay as a Service instances. (https://documenter.getpostman.com/view/5958157/SWDzfMH6?version=latest)

## Current limitations
At this point in time users have to be logged in on the platform in order to receive their own correct data - if they are not logged in the correct SkillSets will be returned, but the progress will be empty.
Other forms of authentication will be introduced in the future.

## Goals and grade calculations

Grades are calculated defined by "Goals", which consist of a number of SkillSets. Those are currently identified by the UniqueID on the SkillDisplay as a Service Server. You can read them from the URI - eg.: https://my.htl3r.skilldisplay.eu/skillset/27 has the UID 27.
 
For each of these SkillSets a grade will be calculated based on the "gradeThresholds" variable.
(You could therefore easily adapt the script for "achievements" or similar use cases)

At this point in time the "value" of certain verifications is set in the same manner as the SkillPoints on the platform:
- Self-Verification ("I claim I know how to do this"): 1 point
- Educational-Verification (Positive written exam on the topic): 2 points
- Business-Verification (Positive practical exercise on the topic): 2 points

## Pull requests
Feel free to introduce pull requests for enhancing the featureset. Ideas include:
- Automatically calculate a total grade, based on the SkillSet grades
- Show users how many Verifications they are missing to reach the next grade 
