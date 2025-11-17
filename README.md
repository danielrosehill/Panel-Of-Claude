# Panel Of Claudes: Experimentary Model For A Multi-Agent Simulated "Debate" (Notes)

Use cases: communications; argument modelling; idea exploration.

## TL;DR

Notes/holding repo for an idea that came to me after having some fun (and learning a bit!) from an experimentary Claude model that approximated the functionality of the CMV (change my view) Subreddit.

My thought was: that was cool. But why not take it further: a subagent takes your viewpoint and buttresses it with research. This is your "advocate."

The next subagent is the CMV subagent.

Finally: when humans assemble panels with divergent viewpoints, there's usually a moderator. Fortunately AI agents can't scream at one another (or wose!) so the role of the moderator here is a bit more civil: it summarises the viewpoints. 

## Implementation: The Panel 

My idea to make this interesting was to try to use context intelligently and sequentially:

- The Advocate gets a pretty barebones articulation of a viewpoint from the user. Like: "trade sanctions have been proven, throughout history, to be ineffective." 
- The Advocate reformats that viewpoint into a prepared "speech": much as if it were preparing for a real debate. 
- CMV agent gets the debate topic and Advocate's speech so that it has a change to rebut its points directly 
- Advocate can add a short closing statement so that both participants have an opportunity to rebut 

The panel "proceedings" get passed to the Moderator: 
- Topic 
- Prompt 
- Speeches

From this, moderator generates a detailed proceedings/minutes of the panel including direct quotes from "speeches."

## Implementation: Outputs 

Outputs:

- JSON for machine-readable outputs 
- Moderator's report as markdown 

Then:

- Markdown to PDF and ePub for reading material 

## Podcast 

- Formatting agent gets the markdown report and formats it into SSML adding the personality of a podcast host 
- SSML gets narrated by TTS 

---

# AI Agent Conference

Potential down the road wacky outgrowths of this idea:

- Agents are instructed to adopt the persona of an ideologue to simulate debates by real personaltiies 
- Multiple panels are assembled as a virtual conference of agents. The minutes from one panel could be fed to another.  
- Responses could be streamed or avatar-ised for live viewing
