#Simple Chat - gives you a chat with AI

Use this for now and run the code to donwload the LLAMA3.1 model
http://localhost:8888/?token=4BByK477-4EVAH-D34DB33F

Visit the chat page here
http://http://localhost:8666/

# Instructions for using the GPU_AMD folder

To use the GPU_AMD folder with AMD GPU support, follow these steps:

1. Navigate to the `Docker/Docker_ChatSimple/GPU_AMD` directory.
2. Run the following command to start the services:
   ```
   docker-compose up
   ```
   (You can add `-d` at the end if you want a long-term service that will remain running on your machine)

3. Visit the front-end at `http://localhost:8080`.
4. Click the settings Icon, Go to Models. Type in a model name like `llama3.1` and hit retrieve.
5. Wait a bit and you're golden.

The `docker-compose.yml` file in the `GPU_AMD` folder is configured to support AMD GPUs using the `rocm` driver.
