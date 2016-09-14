### Image which combines both Yandex AgentNet and OpenAI Gym.
**Only for Python 2.7.**

* To run container, type in command line:
```
docker run -it agentnet-gym bash
```

* To run Jupyter notebook inside container, run:
```
docker run -it -p 8888:8888 agentnet-gym jupyter notebook --ip=0.0.0.0
```
Then, connect to http://localhost:8888 in your browser.
