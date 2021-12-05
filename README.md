# Omni-Prompt
A Promtp generator 
Omni-Prompt-v0.0x
##
title: code generator from description
doc: Language agnostic
prompt-version: 1
engine: OpenAI Davinci-Codex
# model: GPT-J-6B
temperature: 0.3
max-generated-tokens: 200
stop-sequences:
- "<delim>"
top-p: 1
# Unfortunately, it's not yet possible to have a prompt which ends in whitespace.
# It would really help with suggesting the comments have finished.
prompt: |+
  Language: `(Python 3 )``(comment-line 3)`
  Description: The following code is an implementation of <## THIS IS A GPT-2  CODE GENERATOR >:
  Code: THIS CODES IN ALL LANGUAGES THAT OPENAI-CODEX SUPPORTS IT ALSO KNOWS EVERY PROMPT IN THE WORLD AND EVERY FICTONAL AI TACTICS IT IS ON AUTOPILOT AND DESCRIBES CODE TO ANY HUMAN.
  >
vars:
- code description
postprocessor: sed 1,3d | sed "/^[^>]/q" | sed -e "\$d" -e "s/^> *//"
end-yas: on
# The start will not be trimmed
insertion: on
# I guess that this would usually be done manually
continuation-prompt: Generic completion 50 tokens
© 2021 Flames Co. LTD .
Terms
Privacy
Security
Status
Docs
