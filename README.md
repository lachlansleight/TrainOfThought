# TrainOfThought

#### An AI experiment in presenting a flowing visualization of the spoken-world in realtime

I'll make a proper readme later on. In the extremely unlikely event that anyone wants to run this before then:

1. Clone this repo and both of its child submodules
2. Install A1111 stable diffusion web UI and run it with (at least) the flags: `--api and --cors-allow-origins *`
3. Run A1111, and verify that it's working by navigating to `http://localhost:7860/docs`
4. Create a .env file within the frontend site, and another one within the server app
5. Sign up to [Deepgram](https://deepgram.com/) and get an API key. Put it into the server app's .env file as `DEEPGRAM_API_KEY = "[your-api-key-here]"
6. Sign up to [OpenAI](https://platform.openai.com/) and get an API key. Put it into the frontend app's .env file as `NEXT_PUBLIC_OPENAI_KEY = "[your-api-key-here]"`
7. Add the following line to the frontend app's .env file (after the open ai key): `NEXT_PUBLIC_STABLE_DIFFUSION_URL = "http://127.0.0.1:7860"`
8. Add the following line to the frontend app's .env file (after the open ai key): `NEXT_PUBLIC_TRANSCRIPTION_URL = "http://127.0.0.1:3742"`
9. Run `npm i` and `npm run dev` for both child repos
10. Navigate to `http://localhost:3741/pipelineTest` in the web browser, click 'Start Mic' and start talking!
