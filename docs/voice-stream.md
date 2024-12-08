
sudo apt update
sudo apt install pv

curl --proto '=https' --tlsv1.2 -sSf https://sh.rustup.rs | sh

- new terminal
cargo install websocat

cat test1.flac | pv -qL 32000 | websocat --no-close --binary 'ws://localhost:8000/v1/audio/transcriptions?language=en'

-

ffmpeg -y -hide_banner -loglevel quiet -i test2.flac -ac 1 -ar 16000 -f s16le -acodec pcm_s16le audio.pcm
sachin@sachin:~/Music$ ls
audio.pcm  test1.flac  test2.flac
sachin@sachin:~/Music$ cat audio.pcm | pv -qL 32000 | websocat --no-close --binary 'ws://localhost:11800/v1/audio/transcriptions?language=en'

- https://docs.livekit.io/agents/openai/overview/?ref=blog.livekit.io

- https://docs.livekit.io/home/self-hosting/local/

--

curl -sSL https://get.livekit.io | bash


