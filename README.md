# Lecture Atlas

Lecture Atlas listens to a talk and pins every person, place, work, and idea you mention onto a 3D Earth, with its picture, its dates on a timeline, and lines to the other things it is connected to. Students can follow along on their own phones or laptops, and everyone gets a reading list at the end.

Open it here: https://romanf88-arch.github.io/lecture-atlas/

## How to use it

1. Open the page in Chrome or Edge on a computer with a microphone. It does not run in other browsers, because it depends on the speech recognition built into those two.
2. Press **Start listening** and talk. You can also type a sentence in the box at the bottom right.
3. Click any portrait or card to open it. Click the × on a card to remove a wrong pin.
4. **Place names** shows borders, countries, and cities on your globe and on your students' globes.
5. **Topics on** pins names and also general subjects said as ordinary words, such as radium, photosynthesis, or the printing press. Press it to switch to **Topics off**, which pins only the names of people, places, works, and events.
6. **Reading list** collects everything mentioned and saves it as a web page.

## Sharing with students

1. Press **Share with students**. The page shows a QR code, a link, and an 8-character code.
2. Students scan the QR code with a phone, or open the link on a laptop and type the code. The student page works in any browser.
3. The student page has a small globe and a timeline pinned at the top, and a list below them. Each thing you mention appears in all three shortly after it is pinned, with its picture, a short description, and a link to Wikipedia.
   - Students can turn the globe, tap a pin, drag along the timeline, or tap a name. Whatever they choose is shown in all three places.
   - While a student is looking at an older item, new mentions wait, and a "New" button takes them to the latest one.
   - On a phone, the arrow on the globe hides it to leave more room for the list.
   - Place names on a student's globe follow your Place names switch until that student presses the Place names button on their own page.
   - Students can copy or save the list.
4. The student page has no microphone and does not ask for one.
5. The computer keeps the same code until you press **New code**, so you can post the link once for a whole course. **Stop sharing** turns it off.

If you remove a pin or press **Clear**, student pages follow. If you reload the page, students keep the list they already have.

## What it uses

- Listening uses the speech recognition built into Chrome and Edge, which sends audio to the browser maker.
- Names are looked up on Wikipedia. Dates and places come from Wikidata.
- Pictures come from Wikipedia and Wikimedia Commons under their own licenses.
- Country borders come from Natural Earth (public domain).
- Sharing sends the pinned items (title, description, picture link, and dates) through three free public MQTT relay servers: broker.emqx.io, test.mosquitto.org, and broker.hivemq.com. No audio and no transcript are sent. Each update is signed by the presenter's browser, and student pages ignore anything that is not signed with that key.
- No AI service is called while it runs, and the page saves nothing you say.

## Limits

- It needs an internet connection.
- It pins what Wikipedia has an article for. It can miss names Wikipedia treats as ambiguous, and it sometimes pins an ordinary word.
- Dates before year 1 are approximate.
- The relay servers are free public services with no guarantee. They use ports 8084, 8081, and 8884, which some networks block. If the student page says it cannot connect on Wi-Fi, mobile data usually works. Test the student link on the network you plan to use.
- Anyone who has the code can see the list of pinned items.
