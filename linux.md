## kill process with name **sim**
ps -ef| grep sim | awk  '{print $2}' | xargs kill -9
