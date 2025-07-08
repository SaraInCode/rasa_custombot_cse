### Terminal steps to install and run

1. Followed the instructions from `https://rasa.com/docs/pro/installation/python`
2. Observed conflic in faiss-cpu version 1.11.0, which is resolved when installed separately using version 1.10

`uv pip install faiss-cpu==1.10`

3. if server already active , kill it
`netstat -vanp tcp | grep 5005` or `sudo lsof -i :5005` # to list all active in port 5005
`kill -9 <PID>` # kill once PID is found
4. `rasa shell` for cmd line chat
`/stop` to exit cmd line chat
5. `rasa train` to train the model (train after any update)
6. `rasa inspect` to chat in browser mode the trained model
7. How to exit browser chat? (without killing in terminal) ctrl+C 

### Changes Made
1. `domain/domain_global.yml` slots - customer_id - initial_value is updated to `125` from `123` to replicate the screenshot user name
2. `domain/patterns.yml`
