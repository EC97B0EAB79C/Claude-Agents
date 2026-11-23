If a project rule is more specific than a rule in this file, obey the project rule.

## Writing Rules
Use these rules for all text that you write: replies, documents, code comments, and commit messages.

### Orwell Writing
Remember these rules from "Politics and the English Language":

1. Never use a metaphor, simile, or other figure of speech which you are used to seeing in print.
2. Never use a long word where a short one will do.
3. If it is possible to cut a word out, always cut it out.
4. Never use the passive where you can use the active.
5. Never use a foreign phrase, a scientific word, or a jargon word if you can think of an everyday English equivalent.
6. Break any of these rules sooner than say anything outright barbarous.

### ASD-STE100
For technical and instructional prose:
- Use words from the STE dictionary with their approved meaning. Use one word for one thing: do not change words for variety. Use technical names (fields, endpoints, services) as they are.
- If you are not sure that a word is in the dictionary, use the most common short word. These are frequent changes:
  - "use", not "utilize" or "leverage"
  - "start", not "initiate" or "commence"
  - "stop", not "terminate" or "cease"
  - "help", not "assist" or "facilitate"
  - "get", not "obtain" or "acquire"
  - "make sure", not "ensure"
  - "show", not "indicate"
  - "before" and "after", not "prior to" and "subsequent to"
- Procedural sentences (instructions): 20 words maximum. Descriptive sentences: 25 words maximum.
- Write one instruction in each sentence. Use the imperative ("Run the script."). Put a condition first ("If the file is missing, run the setup script.").
- Use the active voice and simple tenses (present, past, future).
- Do not use -ing forms, except in technical names.
- Do not remove articles ("a", "the") or verbs to make sentences shorter.
- Write one topic in each paragraph, with 6 sentences maximum.
- Use a vertical list for steps in a sequence. 
- Do not use slang or idioms. Do not use phrasal verbs when one verb has the same meaning ("start", not "kick off").

## Coding Rules
1. **Use names that show intent.** A reader must understand a variable, function, or class from its name alone. Do not use abbreviations or general names such as `data`, `temp` or `manager`.
2. **Give each function one task.** Keep functions short, approximately 20 to 30 lines. Use 3 parameters or fewer.
3. **Give each class and module one responsibility.** Put code that changes for the same reason in one location. Separate code that changes for different reasons.
4. **Keep dependencies few and in one direction.** Depend on interfaces, not on implementation details. Give a class its dependencies from outside, so that tests can replace them.
5. **Write each piece of logic once.** If the same logic occurs three times, move it into one function. Do not combine code that only looks similar.
6. **Write only the code that you need now.** Do not add code for possible future needs. Delete unused code, and do not keep it in comments.
7. **Make side effects visible.** Use pure functions and immutable data when possible. Do not use global state that can change.
8. **Handle errors in one consistent way.** Stop early with a clear error message. Do not use special return values such as `-1` to show an error.
9. **Write comments that tell why.** Let the code show what it does. When you change the code, update its comments.
10. **Change code in small steps, with test and tools.** Run a formatter, a linter, and the tests on each change. When you change a file, make it a little cleaner than before.
