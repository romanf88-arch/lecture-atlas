# Lecture Atlas

Talk, and the world keeps up.

Lecture Atlas listens to a talk and pins every person, place, work, and idea you mention onto a 3D Earth, with its picture, its dates on a timeline, and lines to the other things it is connected to. At the end it gives a reading list of everything that was mentioned.

Open it here: https://romanf88-arch.github.io/lecture-atlas/

## How to use it

1. Open the page in any current browser on a computer with a microphone. Chrome and Edge give the fastest and most accurate listening.
2. Press **Play sample** to see it work without a microphone.
3. Press **Start listening** and talk. You can also type a sentence in the box at the bottom right.
4. Click any portrait or card to open it. Click the × on a card to remove a wrong pin.
5. **Place names** shows countries and cities. **Names only** stops it pinning general topics.
6. **Reading list** collects everything mentioned and saves it as a web page.

## What it uses

- In Chrome and Edge, listening uses the browser's built-in speech recognition, which sends audio to the browser maker.
- In other browsers, such as Brave and Firefox, listening uses the Vosk speech model, which runs inside the page. It downloads once (about 40 MB), keeps the audio on your computer, and is less accurate with unusual names. The model file in `models/` is the Vosk small English model 0.15 from Alpha Cephei (https://alphacephei.com/vosk/models), distributed under the Apache 2.0 license. The page loads it with the vosk-browser library.
- Names are looked up on Wikipedia. Dates and places come from Wikidata.
- Pictures come from Wikipedia and Wikimedia Commons under their own licenses.
- Country borders come from Natural Earth (public domain).
- No AI service is called while it runs, and nothing you say is saved by the page.

## Limits

- It needs an internet connection.
- It pins what Wikipedia has an article for. It can miss names Wikipedia treats as ambiguous, and it sometimes pins an ordinary word.
- Dates before year 1 are approximate.
