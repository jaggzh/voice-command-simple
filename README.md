# Voice Command - Simple

## Interesting points:
* This project uses https://github.com/jaggzh/whisperpluck
    * Whisperpluck itself either runs OpenAI's whisper (https://github.com/openai/whisper), or keeps a server (found in whisperpluck/server-flask/) running to keep the Whisper model loaded for speed. This specific project (voice-command-simple) requires the server to be up and running. You have to set your paths in the main `patient-command-main` script, and it'll then ensure the whisper server is running.
* This project also uses Piper (https://github.com/rhasspy/piper) for text-to-speech (TTS).  The script `piper-voice-interactive` is a script I wrote to call piper.  You'll also need to look through this script, edit its paths, and .. you'll have to set up piper!  If you want, you can just replace everything in piper-voice-interactive with something that accepts text from STDIN and says it (like `festival --tts`, which accepts from stdin by default).
* Oh, the name `patient-command-main` is because I started writing this for a patient/caregivers to give commands by hitting a button on the keyboard.
* ^ That reminds me, you can run `patient-command-main` directly or you can assign it to a hotkey. It'll speak to you and then listen for 3.5s (currently).
