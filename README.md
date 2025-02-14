# Live AI-generated Real-Time Translation System

> This is a fork of [LiveKit's Live Translated Captioning Example](https://github.com/livekit-examples/live-translated-captioning)

## Watch Tutorial Video

Watch the Implementation Tutorial on YouTube:

<p align="center">
    <a href="[https://youtu.be/gc5NNe7rnFs](https://youtu.be/gc5NNe7rnFs)">
        <img src="https://img.youtube.com/vi/gc5NNe7rnFs/0.jpg" alt="Live Translation Implementation Tutorial" width="560" height="315">
    </a>
</p>

<p align="center">
    <a href="https://www.youtube.com/channel/UCxgkN3luQgLQOd_L7tbOdhQ?sub_confirmation=1">
        <img src="https://img.shields.io/badge/Subscribe-FF0000?style=for-the-badge&logo=youtube&logoColor=white" alt="Subscribe">
    </a>
</p>

## Introduction

This project demonstrates a powerful real-time translation system that automatically transcribes and translates live speech into multiple languages. Perfect for multilingual conferences, educational sessions, or international meetings.

## Key Features

- **Real-Time Translation**: Instant translation of live speech
- **Multi-Language Support**: Currently supports English, French, German, Spanish, and Japanese
- **Single Host System**: Optimized for one speaker with multiple listeners
- **Language Preferences**: Each listener can choose their preferred language
- **High-Quality Speech Recognition**: Powered by Deepgram's advanced STT
- **Neural Translation**: Utilizing OpenAI's GPT-4 for accurate translations

## Technical Stack

- 🌐 **LiveKit**: Real-time communication infrastructure
- 🤖 **LiveKit Agents**: Backend processing and coordination
- 👂 **Deepgram**: Speech-to-text processing
- 🌍 **OpenAI GPT-4**: Neural machine translation
- ⚡ **Next.js**: Frontend framework

## System Architecture

1. **Room Creation & Management**
   - Automatic agent joining on room creation
   - Dynamic host detection and mic stream subscription

2. **Speech Processing Pipeline**
   - Real-time audio streaming
   - Speech-to-text conversion via Deepgram
   - Neural translation processing

3. **Translation Distribution**
   - Language-specific routing
   - Real-time caption delivery
   - Multi-user synchronization

## Running the demo

### Run the agent
1. `cd server`
2. `python -m venv .venv`
3. `source .venv/bin/activate`
4. `pip install -r requirements.txt`
5. `cp .env.example .env`
6. add values for keys in `.env`
7. `python main.py dev`

### Run the client
1. `cd client/web`
2. `pnpm i`
3. `cp .env.example .env.local`
4. add values for keys in `.env.local`
5. `pnpm dev`
6. open a browser and navigate to `http://localhost:3000`

## Known Limitations

- Single host restriction per session
- Occasional UI glitches when multiple browser windows are open
- STT performance may degrade with multiple concurrent connections

## Extending the System

You can easily add support for additional languages by modifying the language configuration in the agent code. The system is designed to be modular and extensible.

## Need Professional Implementation?

Looking to implement a similar system for your organization? Our team at KnoLabs specializes in building custom AI-powered solutions.

🔗 [Contact Us for Professional Implementation](https://knolabs.biz/collect-requirement-page)

## Hosting Partners
- [Kamatera - Get $100 Free VPS Credit](https://knolabs.biz/100-dollar-free-credit)
- [Hostinger - Additional 20% Discount](https://knolabs.biz/20-Percent-Off-VPS)

## Documentation
For more information about LiveKit Agents and their capabilities, visit: [LiveKit Agents Documentation](https://docs.livekit.io/agents/)

## License

This project is licensed under the Apache 2.0 License - see the [LICENSE](LICENSE) file for details.
