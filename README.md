# Duke
AI-powered live and real-time backing track generator.

## Setup
The Duke is a stand-alone. voice-controlled speaker that connects to your wireless network and is powered via USB-C. Some basic setup can be achieved through an app (similar to Sonos speakers) which will include some base-level preferences for genre, tempo, complexity, and entropy. The Duke includes presets for many different genres of music, including blues, jazz, rock, country, and pop.

A custom name can be assigned to the Duke as well, allowing musicians to address the Duke by an alternative name.

Presets consisting of genre, tempo, complexity, and entropy can be created and named.

## Usage
A session begins when you ask Duke to start playing or tell it specifically to begin a new session. A session ends when you stop playing for a configured period of time or tell Duke to end the session. An audible and visual indication will be given before a session is ended automatically.

When the Duke is performing, it is dynamically generating musical instrument lines based on your preferences. The built-in Blues genre, for example, consists of a 4 piece drum set, bass guitar, and rhythm guitar playing a 12-bar progression in 4/4 time in the key of A. All your performance commands will be in the context of the blues framework.

The Duke understands music theory and songwriting practices and will generally follow popular patterns when performing backing tracks. For example, a rock track will start with an intro, two verses with a brief turnaround between them, a chorus, and then repeat verse -> chorus -> verse -> chrouse until you tell it to stop or do something different, such as play a bridge or end the song after the next chorus.

### Session Voice Commands

_"Duke, count me in"_ will begin a session if needed and performa an audible count (based on the current time signature) before starting to play a backing track. You can specify a number of verses or length in minutes as well.

_"Duke, start a new session"_ will stop the current session and start a new one based on the default session preferences.

_"Duke, start a new blues session"_ will stop the current session and start a new one based on the default "Blues" session preferences.

_"Duke, start a new super fast death folk session"_ will stop the current session and start a new one based on the custom "Super Fast Death Folk" session preferences if it exists. If it doesn't, the Duke will use a language model to try and infer your meaning and let you know that it will do what it can.

#### Dynamic Mode
Feel like playing with a bit of fire? Ask the Duke to start a _dynamic_ session. It will listen to your performance and try to anticipate tempo, changes, and modulations as you play! It will use its knowledge of music theory and songwriting to help with this, so if you're playing a blues in A and near the end of the 12-bar pattern you start playing more complex phrases, the Duke will accomodate you by generating more a powerful backing track leading into the next repeat (unless it thinks you're doing this for effect and are expecting a sudden drop in complexity instead).

### Performance Voice Commands
While in a session, you can tell the Duke to change basic settings for the session - for example, _"Duke, change the time signature to 3/4"_ or _"Duke, add a piano and simplify the drum line"_. The Duke will use a language model to determine how to modify the current performance.

The Duke can understand more complex commands as well, such as _"Duke, change to the key of E after the next turnaround"_ and _"Duke, make the arrangmenet more complex over the last 4 bars of this repeat"_. The Duke will use its knowledge of music theory and songwriting to do the best it can.

Even commands like _"Duke, always play two verses before the chorus"_ and _"Duke, play a bridge before every second chorus"_ and _"Duke, end the song with an outro after the next chorus"_ will be acted upon as expected!

## Limitations
The Duke does not have any long-term memory for what it plays, and you cannot repeat a performance. The Duke will create the backing tracks from its music model each time.

The Duke does not learn your style and will make requested and expected changes based on music theory and songwriting knowledge within the session genre. A dynamic session will simulate some deeper insight, but is still just a predictive engine with fuller inputs.

If the Duke can't hear you, it can't help you. Headphones are currently the best solution for this, but noise-cancelling ear-pods can be almost as effective.

By extension, the Duke cannot be automated via MIDI or through the app beyond commands referring to the current session.

There is currently no guarantee that the tracks generated by the Duke are completely free of copyright, so it should not be recorded for any public release and should not be used during a public performance.

There is no facility for custom instruments right now - drum kits are either 4 or 5 piece, guitars have 6 strings, and electronic sounds are basically the public Roland sounds.

## Future Features
Pretty much all of the above limitations will be addressed at some point :)

* performances can be stored and repeated
* the music model will adapt to your style over time
  * voice recognition or explicitly telling the Duke who's running the session will create multiple profiles
* MIDI and app automation; this may include stored performance commands that can still be modified in real-time during performances
* completely copyright free music models and generators
* customize instruments and sounds
  * drum kits with custom cymbals, drums, and sounds
  * guitars (and other stringed instruments) with arbitrary numbers of string and tunings
  * synths and pads!
* rack-mount version for live performances and studios

## Timeline
Oh it'll be a while yet. I'm still learning about AI, LLMs, and music generation. The basic product isn't difficult in itself, but having a reliable backing track generator is tough while the thing hallucinates.
