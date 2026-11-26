---
name: idea-flow
description: The auditor steps for an open request about a large topic. Brainstorm in two rounds, select ideas, make mockups, and get approval. Also used for the mockup steps of Quick ideas.
---
# Idea flow
Do these steps in order. Use the limits of the auditor. Log each delegation in the progress file.

## Steps
1. Send the researcher for the facts of the project. Give it the topic.
2. Round 1: send brainstormer-web, brainstormer-fast, brainstormer-high, and duke at the same time. Give each the topic, the facts, and the limits.
   - If the user asks for no internet access, or the topic has private data, do not send brainstormer-web. brainstormer-high is already in the round.
   - For a large topic, send more than one brainstormer-web. Give each one a different part of the topic.
   - If the topic is large and you do not send brainstormer-web, send more than one brainstormer-high in the same way.
3. Collect the ideas in one numbered list. Do not judge or remove an idea. Do not show which agent gave it.
4. Round 2: send the same brainstormers at the same time. Give each the numbered list. They give feedback and new ideas.
5. Collect the new ideas in the same list. Send the list with the feedback to the planner. The feedback comes from agents that use low or medium effort, so tell the planner to check it. The planner selects the ideas that fit the limits.
6. Check the selection. Make sure that it fits the limits of the request.
   - If it does not fit, send it back to the planner one time with the reason.
   - If it still does not fit, show the ideas to the user with the problem. Ask how to continue.
7. Send one worker (model sonnet) for each selected idea. The task: make a mockup of the idea.
   - If the project rules say where and how to make mockups, follow them. They can ask for a commit with a proposal.
   - If the project has no mockup rules, write the mockup in `.claude/mockups/` of the session folder. Do not commit it. In the mockup task, name the session folder as the **Repository**, because workers run all commands in the Repository of the task.
   - Choose the form from the project: a page for a web app, a screen for a mobile app, sample output for a command-line tool, sample requests and replies for an API.
   - If the project has no user-visible part, use a short text description.
   - Give each mockup worker its own file names, so that two workers never write the same file.
   - Write "Checks: none (do not run the build or the tests)" in the mockup task. The worker checks the mockup itself, for example it opens each image.
8. Show the user each idea name and its mockup path. Ask the user to choose for each idea: approve, change, or drop. Write the question in the "Waiting for user" section.
   - Add the open questions of the planner to this question.
   - If the user drops all ideas, tell the user. Ask if the user wants another round (Idea flow) or to stop.
   - If the user stops, write "Status: done" in the progress file.
9. If the user asks for a change, send it to a mockup worker with the user's words, the mockup path, and the idea. Then ask again (step 8).
   - A change can ask for variants, for example "show 3 places for the icon".
   - Write each round in the "Ideas" section of the progress file.
10. If the project rules want mockups in a commit (for example with a proposal), commit the mockups of the approved ideas now. Do this before the code.
    - Then continue with step 4 of the auditor Procedure. The architect uses model opus. Give it each approved idea.
