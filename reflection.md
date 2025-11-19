When we approached this project, we evaluated our options and chose to continue focusing on the existing typewriter procedures based on the potential for expansion and reuse. We then created additional procedures focusing on long term typewriter use, care, and maintenance that could address a variety of audience types, ranging from beginning typewriter users to advanced enthusiasts. We then tailored the existing user scenarios so that we could have one scenario to address each type of user - novice, intermediate, and advanced. 

The two biggest obstacles we had to overcome were deciding how to break up the procedures into task topics in a way that both made logical sense and worked well for reuse purposes, and differentiating opportunities for concept material from that of reference material. We first decided to narrow our project scope to focus on a specific typewriter. After some research, we settled on a 1957 Smith Corona Sterling, which is a portable, manual typewriter. This allowed us to reduce ambiguity in procedure writing, particularly when discussing particular components of the typewriter and steps to take when conducting maintenance or repairs. To address the first issue, we sat down as a group and drafted a map for our final user guides that would address common needs of our user types. This resulted in breaking the tasks down significantly, so that they could be easily worked into each map that required certain substeps. We then went through all of the procedures, and discussed as a team how we viewed the concept versus reference material. Ultimately, we decided to include most notes, warnings, tips, and additional information in concept topics, while reserving technical definitions and material types for reference topics.

For our beginner user, Genesis, we decided to focus on rudimentary tasks, such as choosing paper, loading paper, and setting margins and line spacing. We then selected concept topics that would best prepare the user with the necessary background information on important typewriter mechanisms, available line spacing options, and additional tips and tricks to consider when setting margins. These tasks and concepts were then supplemented with reference material that covered the different components of a typewriter and their definitions, common formatting used on a typewriter, and different paper types to use.

For our intermediate user, Park, we selected common tasks that were needed for long-term typewriter usage, such as frequent replacement and cleaning tasks. Lastly, for our advanced user, Hunter, we focused on restoration tasks that are typically conducted only by typewriter experts, and only on a need-based frequency. For these two scenarios, we were able to implement a lot of reuse cases. Some of these reuse cases included concept topics focused on cleaning preparation and warnings, task topics such as removing and replacing the typewriter case, removing key components such as the drawband, mainspring barrel, and platen, and reference materials focusing on case terminology and cleaning materials.

Lastly, we implemented conditional formatting in the form of audience content flags. This was implemented where significant reuse occurred, as some of the reuse tasks and concepts contained excessive information for some users, and just enough for others.

## Lindgren Comments

Overall, this is a great first draft! Well done taking on such a rather large "mini" topic model. `:-)` Please review my overarching comments below, as well as the comments within particular files. It may be best to review all of the comments in respective files via the PR on Github.

- Regarding your mapping work, I would like to see you consider revising the way you are reassembling the topics in some cases. For example, in the Genesis map, you place all of the concepts, then all of the tasks, then references. But, does it make sense to bury the procedure after 6 concept topics? Remember that concept and reference topics support tasks/procedures overall. Consequently, reconsider how some concepts or references may be better placed more specifically before or after certain tasks topics/topic groups. For example, take the following 2 concept topics:
  - Example:
    ```
    <topicref type="concept" href="concepts/c_determining_paper_type.dita"></topicref>
    <topicref type="concept" href="concepts/c_loading-paper-issues.dita"></topicref>
    ```
  - Can these 2 concept topics be more appropriately placed around the loading paper task topics?
    ```
    <topicref type="task" href="tasks/t_remove_paper.dita"></topicref>
    <topicref type="task" href="tasks/t_insert_paper.dita"></topicref>
    ```
  - Consider the same question regarding linespacing or margins. In sum, reconsider how your files should be sequenced.
- You must add `<shortdesc>` elements to your topics, so be sure to do so throughout your model.
- Alerting moves should be implemented more widely across your task topics. See my notes in vivo.
- Elaborate on and reconsider your rationale for your conditional processsing choices. Right now, there are some cases where I am not sure why you would, for instance, filter out certain reference information in a table based on user levels of expertise. See the `r_typewriter_anatomy_definitions.dita` in particular. For example, why would you choose to filter out "Body Screws" from novices and deem it "expert" level only?
- See my comments in some other files, which include suggestions for revision to consider throughout the model.

