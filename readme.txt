#-------------------------------------------------------------------------------------------------------------------------------------------
OLLAMA-Farm
#-------------------------------------------------------------------------------------------------------------------------------------------

Some test Docker Workflows to get your started locally with CPU and GPU.
A more advanced Dev workflow with multi CPU+GPU workers and a load balancer node - also an optional Jupyter dev environment with sample code.

The goal of this project is to ultimately build out some Terraform IAC for Azure (and maybe AWS + GCP if I don't get bored)
By being able to spin up your own private GPT cloud you can reliably do large volumes of work and then shut it down when its not needed.
No one can change the model or take away your weights - fine tune to your hearts content without fear of being #cancelled.

#-------------------------------------------------------------------------------------------------------------------------------------------
How to use? - I just want to chat locally to a modern LLM on my own hardware!
#-------------------------------------------------------------------------------------------------------------------------------------------

If you just want to chat locally with modern LLMS just go to the Docker/Docker_ChatSimple folder
Change to either CPU or GPU directory and run

docker-compose up 

(you can add -d at the end if you want a long-term service that will remain running on your machine)

Visit the front-end at http://localhost:8080
Click the settings Icon, Go to Models. Type in a model name like llama3.1 and hit retrieve
Wait a bit and you're golden.

#-------------------------------------------------------------------------------------------------------------------------------------------
Dev! The wild, wild, west of OLLAMA Farming
#-------------------------------------------------------------------------------------------------------------------------------------------

The Docker/Docker_OllamaFarmDev is a bit more complex, it consists of the following:

- The same webUI (http://localhost:8080) as SimpleChat
- A Jupyter notebook server (http://localhost:8888/?token=4BByK477-4EVAH-D34DB33F) so you can run Python Experiments locally 
- A nginx load-balancer that distributes the AI LLM requests to different workers
- And a pool of workers, by default it's set to 2 GPU workers and 2 CPU workers. The CPU workers are still pretty fast.

Feel free to play around with the docker-compose.yml to enable and disable what you want and use more or less CPU/GPU workers.

At the moment this is all for experimentation and a cheap way to locally play with this setup but it'll ultimately lay the foundation
for the Terraform Cloud versions


