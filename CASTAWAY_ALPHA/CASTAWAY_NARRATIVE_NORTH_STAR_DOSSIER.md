# CASTAWAY — NARRATIVE NORTH STAR DOSSIER
## Canonical Product Vision, Simulation Philosophy, Player Experience, and Development Guardrails

**Purpose of this document:**  
This is the narrative and systems north star for **CASTAWAY**, the Survivor life-simulation game. It is designed to be uploaded into a ChatGPT Project, Claude Project, or other long-running development workspace so that future work can be evaluated against a stable, detailed definition of what CASTAWAY is supposed to become.

This is **not** a backlog, patch log, or implementation spec for one build. It answers a deeper question:

> **What is CASTAWAY, what experience is it trying to create, and what laws must remain true as the game grows?**

Whenever a new feature, rewrite, UI choice, challenge, dialogue system, simulation shortcut, or visual redesign is proposed, compare it against this dossier.

---

# 1. THE ONE-SENTENCE THESIS

**CASTAWAY is a spatial, time-based Survivor life simulation in which a season emerges from eighteen modeled human beings who have bodies, routines, relationships, incomplete information, memories, motives, possessions, fears, plans, and consequences.**

The player does not simply choose from a branching Survivor story.

The player **lives inside a Survivor season**.

The simulation determines the situation.  
The player chooses intent.  
Playable interactions determine execution.  
Other castaways interpret what happened through their own beliefs, relationships, personalities, and incomplete information.  
The season remembers.

---

# 2. THE PLAYER FANTASY

The fantasy is not:

- “manage a Survivor tribe”
- “click through Survivor dialogue”
- “pick the best strategic option”
- “solve a series of Survivor minigames”
- “watch an automated season simulator”
- “play a social-stat spreadsheet”
- “read interactive Survivor fan fiction”

The fantasy is:

> **I was actually there.**

The player should eventually remember a CASTAWAY season the way a real contestant might remember one:

- who woke up before everyone else
- who never helped around camp
- who kept disappearing
- which person they always ended up talking to at the well
- the afternoon they realized two allies were closer than expected
- the challenge they personally blew
- the reward that fractured a relationship
- the person who caught them searching
- the fake idol they planted
- the promise they made and regretted
- the Tribal where the plan changed on the walk over
- the juror they knew they had hurt
- the lie they forgot they had told
- the moment they realized they might actually win

A successful CASTAWAY season should generate anecdotes that feel **owned by the player**, not authored in advance.

---

# 3. THE FUNDAMENTAL DESIGN EQUATION

The foundational CASTAWAY equation is:

**SIMULATION → SITUATION → PLAYER INTENT → EXECUTION → PERCEPTION → CONSEQUENCE → MEMORY**

Every major system should participate in that chain.

### SIMULATION
The world is already moving.

NPCs have locations, activities, plans, physical needs, relationships, information, and goals.

### SITUATION
Those independent systems create a specific circumstance.

Example:

- You are at the shelter.
- Tasha and Marcus have walked toward the well.
- Devon is tending the fire.
- You lost the morning challenge.
- Tribal is tonight.
- You heard a rumor that Marcus wants you out.
- Tasha believes Marcus has an idol, but she is wrong.

### PLAYER INTENT
You decide what you want to do.

Follow them.  
Talk to Devon.  
Search for an idol.  
Rest.  
Gather firewood.  
Approach an ally.  
Do nothing and observe.

### EXECUTION
Your intent may involve:

- movement
- timing
- a conversation
- a challenge interaction
- a search interaction
- a physical minigame
- an uncertainty check
- character capability
- player skill

### PERCEPTION
People do not react to omniscient truth.

They react to:

- what they saw
- what they heard
- what they were told
- what they suspect
- what they misinterpreted
- who they trust

### CONSEQUENCE
Relationships, plans, physical conditions, possessions, targets, and opportunities change.

### MEMORY
Important events remain part of the season.

The game should remember enough that later behavior feels causally connected to earlier life.

---

# 4. THE TEN CORE LAWS OF CASTAWAY

These are constitutional rules.

## LAW 1 — No important action exists in isolation

A meaningful action may be:

- witnessed
- interrupted
- overheard
- discovered later
- misinterpreted
- remembered
- lied about
- exploited
- forgiven
- exposed
- weaponized at Tribal
- referenced at Final Tribal Council

If a system routinely allows important actions to occur in sealed bubbles, it is fighting the design.

## LAW 2 — World truth, player knowledge, and NPC belief are different things

This distinction must never collapse.

### World Truth
What is objectively true in the simulation.

Examples:

- Marcus possesses an idol.
- Tasha intends to vote Devon.
- Devon and Marcus have a Final Three agreement.
- An idol is hidden near the eastern trail.
- Caleb lied during a conversation.

### Player Knowledge
What the player reasonably knows.

Player-facing information may be:

- **Known**
- **Suspected**
- **Rumored**
- **Unknown**

The UI must not leak omniscient simulation state merely because the engine internally knows it.

### NPC Belief
Each NPC has their own understanding of reality.

A castaway can:

- know something true
- believe something false
- suspect something without proof
- trust a liar
- distrust someone telling the truth
- hear an outdated plan
- misremember a conversation
- spread bad information

A false belief can be strategically real because people act on beliefs.

## LAW 3 — Relationships are directional and multidimensional

“Relationship = 72” is insufficient.

A can like B without trusting B.  
A can trust B without respecting B.  
A can dislike B while believing B is reliable.  
A can fear B strategically while loving B personally.

A directional relationship may track:

- affection
- trust
- loyalty
- strategic respect
- fear
- resentment
- jury respect
- perceived threat
- social closeness
- reliability estimate
- recent emotional momentum

A → B does not have to equal B → A.

This asymmetry creates real social texture.

## LAW 4 — NPCs live when the player is not looking

Other castaways cannot freeze offscreen.

They:

- travel
- work
- rest
- talk
- strategize
- search
- practice
- eat
- gather resources
- form groups
- leave groups
- make promises
- share rumors
- change targets
- find things
- miss things
- get annoyed
- reconcile
- become suspicious

The player is a participant in the world, not the CPU around which the world revolves.

## LAW 5 — The season remembers

Important experiences become persistent memories.

Examples include shared food, reward inclusion/exclusion, idol-hunting suspicion, promises, betrayals, secrets, alliance formation/exclusion, challenge heroics/failures, comfort, conflict, bag searches, and discovered deception.

Memories can carry:

- emotional weight
- strategic weight
- secrecy
- witnesses
- longevity
- relevance

Some decay. Others become defining.

## LAW 6 — Identity changes affordances, not destiny

A castaway’s life background must matter mechanically.

Examples:

- parent → specific bonding opportunities
- carpenter → shelter insight
- teacher → patience/coaching options
- fishing hobby → richer fishing options
- athlete → different physical challenge confidence
- poor swimmer → tighter swim execution margins
- Survivor superfan → greater structural familiarity

No life fact guarantees success.

Identity changes opportunities, interpretation, confidence, and probabilities.

## LAW 7 — Player skill and character capability both matter

CASTAWAY is not purely statistical and not purely twitch-based.

Character capability and player execution should both affect many playable tasks.

A weak castaway should not become a physical god because the player has excellent reflexes.

A skilled player should not feel that every challenge is a hidden dice roll.

## LAW 8 — Time is a resource

Every meaningful action consumes time.

Choosing one thing means potentially missing another.

If you search for an idol:

- someone else may bond at camp
- an alliance may form without you
- someone may notice you are gone
- you may miss a rumor
- your work reputation may suffer
- the person you wanted to talk to may move

Travel itself can consume time.

Opportunity cost is one of CASTAWAY’s central tensions.

## LAW 9 — Prefer state-driven events over scripted branches

The engine should ask:

> “Given who these people are, what they know, how they feel, where they are, and what just happened, what becomes likely now?”

It should not usually ask:

> “Has the player reached Story Scene 7?”

Production structure can be scheduled. Human drama should emerge from state.

## LAW 10 — The story engine recognizes stories; it does not force them

The simulation produces events.

A story layer may later recognize:

- rivalry
- revenge
- underdog survival
- loyal pair
- social connector
- challenge comeback
- idol hunter
- alliance betrayal
- secret keeper
- reconciliation
- rise and fall

Those labels can improve confessionals, recaps, episode summaries, jury references, and FTC.

They must not force events into existence.

**Drama should be discovered, not scheduled.**

---

# 5. CASTAWAY IS A SPATIAL LIFE SIMULATION

The eventual primary play space is a stylized explorable Survivor world.

Canonical kinds of locations include:

- Shelter
- Fire
- Well
- Beach
- Jungle
- Fishing Spot
- Tree Mail
- Confessional
- Idol-search areas
- Challenge Path
- Tribal Path
- Challenge Arena
- Tribal Council

These are not decorative navigation labels.

Location affects:

- who can be encountered
- who can witness
- what actions are available
- privacy
- travel time
- overhearing
- interruption
- resources
- environmental exposure
- risk

Someone cannot simultaneously be at the well, idol hunting in the jungle, speaking at shelter, and witnessing an event at the beach.

**Physical presence is authoritative.**

---

# 6. TIME AND MOVEMENT ARE PART OF THE GAME

CASTAWAY uses a real day clock.

Time flows through:

- activities
- conversations
- movement
- challenges
- medical events
- searching
- rest
- camp work
- meals
- ceremonies

The exact production schedule can vary.

The key principle is:

> **The world advances while the player acts.**

NPC schedules advance at the same time.

A long conversation is a real time commitment.

Walking into the jungle is a real movement commitment.

Searching creates an interval during which other things can happen.

---

# 7. LIVING CAMP

The camp should feel occupied by people with lives.

The Living Camp direction establishes a core NPC loop:

**DECIDE → TRAVEL → OCCUPY → COMPLETE / INTERRUPT → RECONSIDER**

NPC behavior should not resemble random teleportation between activity labels.

A castaway who decides to fetch water should:

1. form that intent
2. move toward the appropriate location
3. arrive
4. perform the action
5. remain occupied for meaningful time
6. finish, get interrupted, or reprioritize
7. form a new intent

NPCs may choose activities including water collection, firewood, fire tending, shelter work, food gathering, fishing, cooking, resting, swimming, fire practice, idol searching, strategizing, socializing, following, observing, and seeking privacy.

The next evolution is **routine identity**.

Over days, castaways become recognizable through habits:

- waking early
- working before socializing
- hanging around the fire
- disappearing after setbacks
- gravitating toward certain locations
- avoiding labor
- searching more when paranoid
- seeking company when afraid
- isolating after conflict

These are weighted tendencies, not scripted schedules.

**People have habits, not railroads.**

---

# 8. SOCIAL GRAVITY

Humans do not select social targets independently every five minutes.

Relationships should create gravitational patterns.

Castaways may:

- seek a particular ally
- naturally work near a friend
- linger around a group
- avoid an enemy
- follow a suspicious person
- try to catch someone alone
- attempt to break into a cluster
- abandon one conversation for another
- feel excluded by recurring groups
- become annoyed that two people are always together

Recurring physical clustering is strategically meaningful.

The player should be able to notice:

> “Those three are always together.”

without receiving an omniscient **ALLIANCE DETECTED** popup.

Observation is gameplay.

---

# 9. CONVERSATION: THE “SURVIVOR WESTWORLD” PRINCIPLE

Conversation is one of CASTAWAY’s defining systems, but it is **an activity inside the world**, not the entire game.

Conversation must be specific to:

- speaker identity
- life facts
- personality
- current emotion
- current strategy
- relationships
- memories
- secrets
- recent events
- actual knowledge
- location
- privacy
- nearby people
- interrupted activity
- time
- proximity to Challenge or Tribal

Avoid generic loops such as:

- “What’s going on?”
- “Talk strategy.”
- “Get personal.”
- “Build trust.”
- “You had a good conversation.”

Conversation possibilities should include mundane camp talk, jokes, teasing, storytelling, family, career, food, fear, boredom, frustration, flirtation, vulnerability, gossip, strategy, alliance talk, target discussion, information trading, lying, partial truth, confrontation, apology, silence, awkwardness, subject changes, and voluntary endings.

A conversation may stall.

Someone may refuse to discuss strategy.

A person may be too tired.

A third person joining should change what can safely be said.

The player leaving should not freeze the remaining conversation.

People may continue talking after you walk away.

**You do not automatically know what they say.**

---

# 10. KNOWLEDGE IS LOCAL

Internally, the engine may know every location, target, alliance, idol, rumor chain, and relationship score.

The player should not.

UI language should distinguish:

- **KNOWN**
- **SUSPECTED**
- **RUMORED**
- **UNKNOWN**
- **LAST SEEN**
- **OUT OF SIGHT**

A camp panel must never say:

> “Marcus — idol searching in east jungle”

if the player has no reason to know that.

It might say:

> “Marcus — last seen leaving the shelter 18 minutes ago.”

or:

> “Marcus — out of sight.”

**The simulation can be omniscient. The interface cannot.**

---

# 11. PERCEPTION, WITNESSING, AND OVERHEARING

Events require physical and informational context.

A witness generally requires:

- plausible spatial presence
- enough perception
- visibility or audibility
- no disqualifying offsite/phase state

Witnessing can be partial.

Someone may:

- clearly see an event
- hear fragments
- notice suspicious body language
- infer something
- misunderstand
- miss the crucial detail

Example:

You and Marcus whisper near the fire.

Devon may not hear the plan but may notice:

> “Danny and Marcus suddenly stopped talking when I approached.”

That observation can become knowledge.

---

# 12. INTERRUPTION IS A FIRST-CLASS SYSTEM

Long actions should create interruption windows.

Example idol search:

1. player enters a search area
2. time advances
3. NPC routines continue
4. someone’s path intersects the area
5. an interruption becomes possible
6. player may continue, hide, bluff, listen, abort, follow, or confront
7. witnesses and beliefs update

The same concept applies broadly.

A conversation can be interrupted.

Camp work can be abandoned.

Someone can stop walking because they see something interesting.

An alliance meeting can dissolve because another person appears.

CASTAWAY becomes alive when plans collide.

---

# 13. PEOPLE ARE MODELED HUMANS, NOT ARCHETYPES WITH SKINS

A castaway should possess a coherent Human Blueprint.

### Identity
- id
- name
- pronouns
- age
- hometown
- occupation
- tribe
- game status

### Life Facts
- family
- hobbies
- fears
- outdoor experience
- athletic history
- swimming comfort
- puzzle confidence
- professional skills
- Survivor familiarity / fandom type

### Personality
Possible dimensions:
- risk tolerance
- loyalty preference
- strategic aggression
- emotionality
- forgiveness
- willingness to deceive
- social need
- leadership desire
- threat sensitivity
- idol paranoia
- challenge competitiveness
- resource selfishness

### Capabilities
Possible dimensions:
- absolute strength
- relative strength
- endurance
- swimming
- balance
- dexterity
- coordination
- explosive power
- mobility
- grip
- puzzle
- memory
- perception
- survival
- cooking
- fishing
- firemaking
- deception
- persuasion
- composure

### Physical State
- energy
- hunger
- hydration
- morale
- injury
- sleep debt
- illness
- body weight / attrition where appropriate

### Strategic State
- preferred targets
- acceptable targets
- protected people
- perceived majority
- desired voting bloc
- danger list
- idol fears
- suspected alliances
- promises
- secrets
- known information
- uncertainties

Generated people should not feel like random-stat soup.

Traits should create recognizable tendencies.

---

# 14. POLITICAL LIFE: INTENT IS NOT ACTION

Each castaway may hold:

- ideal boot
- acceptable boot
- emergency boot
- protected people
- danger list
- desired coalition
- perceived swing votes
- suspected alliances
- information they want
- information they hide
- current promises
- intended vote

But:

> **A planned vote is not a final vote.**

A person can change because new information arrives, an ally pressures them, idol fear increases, trust changes, a lie is exposed, a new majority becomes plausible, a whisper occurs, they panic, or self-preservation overtakes loyalty.

This volatility is not random.

It is **state change**.

---

# 15. VOTE INTENT

A voter’s preference should emerge from competing pressures:

- personal resentment
- strategic threat
- challenge liability
- challenge value
- alliance requests
- trust
- promises
- revenge
- jury threat
- idol fear
- perceived majority
- fear of exclusion
- personality
- recent memories
- emotional state
- confidence in information

The most likely target need not be perfectly deterministic.

The crucial requirement is:

> **After the vote, the engine should be able to explain why somebody voted the way they did.**

Not with hidden math.

With human causal language.

---

# 16. ALLIANCES ARE SOCIAL OBJECTS, NOT TEAM ASSIGNMENTS

An alliance may track:

- members
- creation time
- secrecy
- cohesion
- shared target
- internal trust
- perceived leader
- memories
- current activity

Alliance membership does not equal loyalty.

A person can be in multiple alliances, secretly defect, leak information, keep an alliance as cover, trust one member more than another, or believe an alliance is more real than the rest of its members do.

“Alliance = true” is never the complete model.

---

# 17. SECRETS, RUMORS, AND INFORMATION

Secrets should exist as world-truth objects known by subsets of people.

Examples:

- idol possession
- beware condition
- planned blindside
- Final Three agreement
- fake idol
- bag search
- advantage possession
- private betrayal plan

A secret can have:

- true owners
- known-by list
- suspected-by list
- false variants
- exposure risk

Information can spread through chains and mutate.

By the time a rumor reaches the fourth person, it may no longer match the original fact.

That is desirable.

---

# 18. IDOLS AND ADVANTAGES MUST BE PHYSICAL

Possessions have physical location and availability.

An idol can be:

- on person
- in bag
- at camp
- in hidden cache
- temporarily held elsewhere

If you leave your bag behind when going to Tribal, an idol stored inside should not magically appear in your pocket.

The broader ecosystem can include Hidden Immunity Idols, clues, Beware Advantages, extra votes, vote steals, Safety Without Power, Shot in the Dark, and other season-appropriate mechanics.

Advantages are interesting because they exist inside secrecy, movement, risk, discovery, and social interpretation.

---

# 19. IDOL HUNTING SHOULD BECOME PHYSICAL GAMEPLAY

Avoid reducing idol hunting to:

> SEARCH FOR IDOL — 30 MINUTES

The direction is spatial.

The player physically leaves camp.

That departure can be noticed.

Searching consumes time.

Areas may contain clues, environmental hints, false leads, hidden objects, or evidence another person searched there.

NPCs search independently.

Lightweight skill interactions can eventually support the search.

The important part is not the QTE.

The important part is:

> **Searching happens in a world with other people.**

---

# 20. BAGS, FAKE IDOLS, AND PHYSICAL DECEPTION

CASTAWAY should support physical Survivor deception where season rules permit it.

Examples:

- search someone’s bag
- get caught searching
- learn information
- hide an idol
- move an item
- craft a fake idol
- use camp materials/beads
- plant a fake
- discover a fake
- believe a fake is real

These systems become meaningful because knowledge is local and memory persists.

---

# 21. CAMP SURVIVAL IS NOT DECORATION

The body matters.

Camp life should affect:

- hunger
- hydration
- fatigue
- sleep debt
- injury
- illness
- morale
- weight loss / attrition
- challenge performance
- emotional regulation where appropriate

Camp systems can include fire, shelter, water, fishing, food, cooking, gathering, weather, rest, and medical events.

NPCs participate.

A person who consistently works may gain a reputation.

A person who never works may develop one too.

---

# 22. REPUTATION SHOULD EMERGE FROM OBSERVED BEHAVIOR

Do not simply assign:

> PROVIDER = +20

People should form opinions because of repeated experiences.

Examples:

- who works
- who is lazy
- who eats disproportionately
- who disappears
- who constantly strategizes
- who helps injured players
- who starts conflict
- who performs under pressure
- who comforts others
- who lies

Reputation depends on **observation and information**.

If nobody relevant sees your contribution, the social credit may be lower.

---

# 23. CHALLENGES ARE PLAYABLE, VARIED, AND PHYSICAL

Challenges should not collapse into one generic QTE.

The challenge framework should support distinct interaction identities:

- timing
- balance
- analog / omnidirectional movement
- dual virtual sticks
- tilt mechanics
- optional device motion
- rope manipulation
- grab / slack / tension
- threading
- hauling
- knot interactions
- obstacle movement
- firemaking
- puzzles
- memory
- physical tasks

Controls should support:

- touch-first
- controller-first
- mouse/keyboard

Optional enhancements:

- controller rumble
- richer mobile haptics
- gyroscope / accelerometer

Haptics must never be required.

---

# 24. THE TILT-MAZE EXAMPLE

A favored challenge interaction is a physical tilt maze where three balls must be guided into holes.

Preferred approach:

- two virtual control sticks
- one on each side
- tuned omnidirectional tilt
- analog-feeling balance
- simple readable visual design
- lightweight physics
- nearby competitor progress visible where useful

Future optional mode:

- physically tilt an iPad/device

Dual virtual sticks remain the accessible fallback.

This represents a broader principle:

> **CASTAWAY challenges should feel tactile without requiring AAA visual complexity.**

---

# 25. ROPE PHYSICS DIRECTION

Rope should be a reusable physical challenge primitive.

Desired interactions:

- grabbing
- dragging
- slack
- tension
- posts
- loops
- threading
- hauling
- knots
- future pulleys
- cargo interactions

The point is physical reasoning and tactile control, not graphical spectacle.

---

# 26. CHALLENGE PERFORMANCE BELONGS TO THE CASTAWAY

The player participates through their avatar.

A stronger castaway may move weight more efficiently.

A better-balanced castaway may have more forgiving stability.

A better puzzle solver may get stronger margins or AI speed.

Exact implementation can vary.

The law remains:

> **You are playing through a person, not controlling a disembodied cursor.**

---

# 27. OTHER COMPETITORS EXIST DURING CHALLENGES

When a challenge is simultaneous, the player should feel other castaways progressing.

Where appropriate show:

- nearby bodies
- lane progress
- status markers
- competitor milestones
- live standings

Avoid making every challenge feel like an isolated single-player minigame compared after the fact.

---

# 28. TRIBAL COUNCIL IS AN EVENT, NOT A RESULTS SCREEN

Tribal should eventually be experienced.

Potential stages:

- leaving camp
- Tribal path
- arrival
- seating
- opening questions
- reactions
- information exposure
- confrontation
- live uncertainty
- whispers where rules allow
- voting
- advantage / idol window
- vote reveal
- elimination
- torch snuff
- return to camp

Questions matter because answers affect beliefs, relationships, threat perception, trust, and jury memory.

Tribal does not merely calculate what happened earlier.

It is itself part of the game.

---

# 29. THE WALK TO TRIBAL CAN MATTER

The transition to Tribal should preserve physical continuity.

Avoid:

> click TRIBAL → teleport → reveal result

The journey can create tension, silence, last-minute looks, and uncertainty.

Not every walk needs interaction.

The world simply should not feel discontinuous.

---

# 30. VOTE REVEALS NEED CAUSAL LEGIBILITY

After the vote, the game should internally be able to reconstruct:

- who voted for whom
- what they believed
- which conversations affected them
- what alliance pressure existed
- what fears mattered
- what memories mattered
- what advantage changed the result

This does not mean exposing every hidden variable immediately.

It means preserving causal traceability for recaps, confessionals, and future jury references.

---

# 31. MERGE CHANGES THE SOCIAL GEOMETRY

At merge:

- tribal partitions end
- old tribal relationships remain
- cross-tribe connections become possible
- challenge threat becomes individual
- jury management grows
- shields, goats, swing votes, and blocs become more dynamic
- clustering patterns change

Merge is more than `merged = true`.

It changes the social space.

---

# 32. ENDGAME

The endgame preserves the same simulation principles.

Important late-game concepts:

- individual immunity
- threat management
- shields
- goats
- voting blocs
- jury perception
- jury relationships
- Final Five
- Final Four
- firemaking where format requires it
- Final Tribal Council

Late-game strategy should emerge from accumulated history.

---

# 33. FINAL TRIBAL COUNCIL MUST REMEMBER THE SEASON

FTC is not a final score check.

Jurors can arrive:

- angry
- hurt
- impressed
- bitter
- confused
- forgiving
- disappointed
- confrontational
- checked out
- emotionally conflicted

When earned by the season, FTC should support old-school Survivor intensity:

- accusations
- incorrect assumptions
- accountability demands
- dramatic speeches
- moral questions
- personal disappointment
- crashouts
- reconciliation
- respect

The player should respond in real time.

Possible responses:

- own a move
- apologize
- push back
- correct a misconception
- reveal hidden information
- explain motive
- defend betrayal
- acknowledge harm
- expose another finalist’s action

A juror can be factually wrong.

The player may have to decide whether correcting them helps.

FTC should feel like **the accumulated season becoming conversationally present**.

---

# 34. JURY MANAGEMENT STARTS BEFORE FTC

Jury votes should not be generated from a fresh endgame formula.

Jurors remember:

- relationships
- promises
- betrayals
- respect
- challenge performance
- social treatment
- arrogance
- humility
- exclusion
- reward choices
- emotional moments
- strategic agency
- later information

The jury is not a scoreboard.

It is a group of people with memories.

---

# 35. PONDEROSA / ELIMINATED-LIFE DIRECTION

A future playable Ponderosa layer can preserve the world after elimination.

Possible experiences:

- juror relationships
- decompression
- discovering hidden information
- messages/calls from home
- post-game conversations
- emotional fallout
- jury opinion evolution
- fan/media/podcast-style social elements where appropriate

This is secondary to the main game, but fits the life-sim philosophy.

---

# 36. CONFESSIONALS

Confessionals help the player and game make meaning from the season.

They can support:

- reflection
- emotion
- strategic explanation
- story recognition
- player personality expression
- production-style recap

They must not become omniscient exposition.

A confessional represents what the castaway thinks, not what the engine knows.

---

# 37. THE STORY ENGINE

The story engine is retrospective and interpretive.

It may identify arcs such as:

- rivalry
- underdog survival
- alliance betrayal
- idol hunter
- challenge comeback
- loyal pair
- secret keeper
- revenge
- social connector
- rise and fall
- reconciliation

These tags can improve episode summaries, recaps, confessionals, FTC references, and post-game history.

The story engine must never force a plot beat merely because the label exists.

---

# 38. PRODUCTION STRUCTURE VS HUMAN EMERGENCE

CASTAWAY can have structured Survivor production:

- Pregame
- Marooning
- tribes
- challenges
- rewards
- Tribal Councils
- merge
- twists
- jury
- finale

These provide **external structure**.

Inside that structure, human outcomes remain emergent.

> Production schedules the arena.  
> People create the season.

---

# 39. PREGAME MATTERS

Pregame is not irrelevant setup.

It is the first opportunity for:

- first impressions
- observation
- body-language reads
- assumptions
- nervousness
- curiosity

Full interaction may be restricted depending on the production scenario, but people can begin forming beliefs.

The season begins before Day 1.

---

# 40. DAY 1 MUST FEEL LIKE ARRIVAL, NOT MIDSEASON

A fresh campaign must not inherit future knowledge, items, advantages, or relationships.

Day 1 should feel like:

- uncertainty
- orientation
- introductions
- first work
- first impressions
- shelter/fire concerns
- early social grouping
- people learning the island

The game must not spawn into a world that behaves as though several episodes already occurred.

---

# 41. THE FIELD-TERMINAL UI

CASTAWAY’s secondary information layer uses a rugged Survivor production / expedition field-device aesthetic.

Desired qualities:

- practical
- weathered
- expedition-oriented
- readable
- Survivor-production adjacent
- functional
- compact

Avoid:

- Fallout imitation
- nuclear styling
- military sci-fi
- cyberpunk
- meaningless fake sectors
- green-monochrome gimmickry

The interface exists to help the player understand their lived situation.

---

# 42. UI IS SECONDARY TO THE WORLD

The long-term primary experience is spatial.

The field terminal can support:

- status
- inventory
- map
- relationships
- known information
- journal
- confessionals
- challenge information
- saves
- production notices

But the terminal must not swallow the game.

A feature is not complete merely because there is a good panel for it.

If an activity should happen physically in the world, eventually the player should experience it there.

---

# 43. VISUAL WORLD DIRECTION

The world is being developed through a separate **CASTAWAY World Lab / Modeling School** pipeline.

That work includes:

- terrain
- shoreline
- water
- rocks
- logs
- poles
- rope
- palm fronds
- palm trees
- shelter
- camp composition
- character scale
- human body mesh
- hands
- heads
- clothing
- rigging
- animation

The World Lab is visual/spatial R&D for CASTAWAY.

It should not redefine the simulation philosophy.

The simulation and presentation pipelines can advance in parallel and later converge.

---

# 44. CHARACTER VISUAL DIRECTION

The desired character direction is stylized rather than photoreal.

The game needs:

- readable bodies
- human proportions
- expressive silhouettes
- believable hands
- recognizable heads/faces
- practical rigging
- animation-friendly topology
- enough individuality for eighteen castaways

Facial and body readability matter because proximity, reactions, body language, and group composition matter.

The goal is not maximum polygon count.

The goal is convincing human presence.

---

# 45. SCALE AND PERFORMANCE PHILOSOPHY

CASTAWAY does not need Roblox-level or AAA 3D complexity.

The simulation sophistication can exceed the rendering sophistication.

Prefer:

- readable stylization
- efficient assets
- lightweight physics
- intentional animation
- tactile interactions
- stable performance

over graphical spectacle that reduces systemic depth.

---

# 46. SAVE STATE IS THE SEASON

Saving must preserve enough state that loading feels like resuming reality.

Relevant save state includes:

- world time
- RNG/deterministic stream where used
- castaways
- conditions
- locations
- activities
- relationships
- knowledge
- memories
- alliances
- inventories
- advantages
- secrets
- camp objects
- season structure
- challenge state where appropriate
- story/history
- current commitments

A save/load operation must not resurrect eliminated players, duplicate identities, invent items, leak future state, reset important relationships, or re-roll the past.

---

# 47. DETERMINISM: THE PAST IS FIXED

Where deterministic simulation is used, loading a save should restore the same state and random stream.

The future should change because the player makes different choices—not because loading arbitrarily rerolls history.

This improves debugging, fairness, causal reasoning, and player trust.

---

# 48. MEDICAL AND PHYSICAL CONSEQUENCES

Players and NPCs can suffer:

- exhaustion
- injury
- illness
- dehydration
- hunger
- sleep deprivation
- challenge-related consequences

Medical events should come from believable state and can interrupt activities, strategy, travel, challenges, and camp routines.

A medevac or serious injury should feel causally rooted.

---

# 49. REWARDS

Rewards should be life events, not inventory popups.

Possible consequences:

- food
- cultural experiences
- camp supplies
- letters/messages from home
- comfort
- isolation from camp
- relationship effects
- overeating sickness
- intoxication where thematically appropriate
- truth-control/social consequences
- choosing attendees

Who gets chosen matters.

Who gets excluded matters.

The people left at camp continue living.

---

# 50. ORDINARY SURVIVOR LIFE IS CONTENT

CASTAWAY does not need a twist every five minutes.

Important moments can be:

- gathering wood
- sitting around a fire
- fishing
- arguing about rice
- lying in the shelter
- getting soaked
- waking up miserable
- talking about family
- being bored
- noticing two people whispering
- laughing at something stupid

Ordinary life gives strategic moments context.

Without ordinary life, the season becomes a sequence of mechanics.

---

# 51. DRAMA REQUIRES QUIET

Do not optimize every minute for maximum conflict.

A believable social world needs:

- calm
- routine
- humor
- silence
- boredom
- work
- companionship

Then betrayal means more.

---

# 52. PLAYER AGENCY

CASTAWAY should not tell the player how to play Survivor.

The player can attempt to be:

- loyal
- ruthless
- social
- quiet
- chaotic
- provider
- challenge-first
- idol-focused
- alliance-heavy
- under-the-radar
- confrontational
- deceptive

The simulation responds.

There should not be one hidden “correct strategy.”

---

# 53. FAILURE IS PART OF THE EXPERIENCE

The player should be allowed to:

- misread a person
- waste time
- lose a challenge
- get caught searching
- trust the wrong ally
- play an idol incorrectly
- miss a conversation
- anger someone
- make a bad promise
- become the target
- get voted out

The game is not obligated to rescue the player from a bad season.

That risk is central to Survivor.

---

# 54. INFORMATION SHOULD BE INFERABLE

Incomplete information must not become arbitrary opacity.

The player should be able to observe clues:

- recurring groups
- strange absences
- changed behavior
- nervousness
- body language
- inconsistent stories
- voting patterns
- whispered conversations
- sudden friendliness
- resource behavior

A strong player should become better at reading the world.

CASTAWAY is not a guessing game.

It is an **observation game**.

---

# 55. NPC INTELLIGENCE SHOULD BE HUMAN, NOT PERFECT

NPCs should not know everything, calculate perfectly, optimize instantly, coordinate magically, or never forget.

They may:

- overreact
- underestimate
- misread
- panic
- become stubborn
- act loyally against strict strategic interest
- forgive
- refuse to forgive
- believe a friend
- make an ego move

Human imperfection is part of simulation quality.

---

# 56. NPCS NEED INTERNAL CAUSALITY

When an NPC does something surprising, the engine should ideally answer:

> Why?

Example:

“Why did Tasha leave the majority?”

Because:

- she trusted Devon less after he exposed her secret
- she believed Marcus had an idol
- she felt excluded from the reward
- Caleb offered a Final Three
- she perceived the vote as moving
- self-preservation outweighed loyalty

The player may not know every cause.

The simulation should.

---

# 57. NPC AUTONOMY MUST NOT BECOME CHAOS

Emergence needs constraints.

NPC behavior must respect:

- current phase
- physical location
- travel time
- tribe membership
- elimination status
- production events
- injury
- activity occupation
- conversation participation
- challenge attendance
- Tribal attendance

A “smart” AI that violates the physical world is worse than a simpler AI that respects it.

---

# 58. AUTHORITY PRINCIPLE

For any stateful concept, there should be a clear source of truth.

Examples:

- one authoritative location
- one authoritative activity
- one authoritative phase
- one authoritative season schedule
- one authoritative elimination status
- one authoritative possession location

Avoid parallel systems that both believe they own the same fact.

This is one of the major architectural lessons from the 0.3.109 hardening era.

---

# 59. THE 0.3.109 LESSON

CASTAWAY went through extensive hardening around:

- save integrity
- Pregame authority
- early-game authority
- Day 1 spatial continuity
- travel
- physical presence
- offsite perception
- witness logic
- tribe presence
- phase boundaries
- political knowledge
- jury authority

The deeper lesson was not merely “remove bugs.”

It established:

> **The world must agree with itself.**

If an NPC is offsite, one system cannot still treat them as a camp witness.

If someone is traveling, they cannot already be performing the destination activity.

If the season is Day 1, no future-state advantage should exist unless intentionally created.

Future features must preserve that consistency.

---

# 60. TESTING PHILOSOPHY

Do not return to infinite paranoid bug checking after every small change.

Recommended cadence:

### For each feature
1. implement
2. targeted regression test
3. short trunk smoke test
4. move forward

### After several major milestones
Run a broader deep audit.

### Major beta milestone
Play an uninterrupted season without debug skips.

Track:

- boredom
- confusion
- fake-feeling NPC behavior
- magical information
- broken consequences
- dead time
- drama that should happen but does not
- systems that technically work but are not fun

A real season playthrough eventually teaches more than endless micro-fuzzing.

---

# 61. CURRENT DEVELOPMENT ERA: MAKE THE SIMULATION VISIBLE

The underlying simulation is increasingly sophisticated.

The next objective is not simply adding more hidden variables.

It is turning them into lived experience.

## 0.3.110 — Living Camp
Make NPC lives visible and persistent.

### Foundation
- commitments
- travel
- activity occupation
- completion
- interruption
- reevaluation

### Routine Identity
- habits
- activity bias
- preferred people
- preferred places
- changing tendencies

### Social Gravity
- seeking
- avoiding
- recurring clusters
- group formation
- exclusion

### Interruptions & Opportunism
- reacting to nearby events
- changing plans
- investigating behavior
- joining/leaving groups

### Camp Memory & Reputation
- work reputation
- suspicious absences
- social behavior
- observed contribution
- repeated patterns

Then:

## 0.3.111 — Conversation 2.0
Fuse the living world with deep contextual dialogue.

This is the bridge between “the simulation works” and “the player feels like they are living on Survivor.”

---

# 62. WHAT CASTAWAY MUST NEVER BECOME

## Do not turn CASTAWAY into a menu clicker

If the optimal interaction becomes:

1. open menu
2. click STRATEGIZE
3. receive relationship points
4. click SEARCH
5. receive idol chance

the life-sim fantasy collapses.

Menus can support the world.

They should not replace it.

## Do not turn CASTAWAY into a visual novel

Dialogue is important.

But a Survivor season contains movement, observation, work, physical risk, challenges, hardship, searching, silence, and boredom.

Conversation cannot be the entire interface.

## Do not turn CASTAWAY into a spreadsheet simulator

Deep state is good.

Visible raw state is not automatically good.

The player should experience:

> “I think Marcus doesn’t trust me anymore.”

not necessarily:

> TRUST: 43.7 → 39.2

Raw diagnostics can exist for development.

The player-facing game should privilege human interpretation.

## Do not turn CASTAWAY into a scripted story

Never guarantee a villain, betrayal, showmance, underdog, or blindside.

Allow them.

Recognize them.

Do not require them.

## Do not turn NPCs into omniscient agents

They cannot act on secret information they never learned, events they did not witness, hidden inventory they have not discovered, or future votes.

Every knowledge-sensitive decision must have an informational path.

## Do not teleport people casually

Movement matters.

Instantaneous presence changes can destroy witnessing, timing, interruption, secrecy, and opportunity cost.

Use explicit travel where physical continuity matters.

## Do not make every action predictable

Strong systems need uncertainty.

But uncertainty should come from other humans, imperfect information, physical execution, environment, emotion, and legitimate randomness—not arbitrary outcome roulette.

## Do not make every action dramatic

Normal life is required.

A camp where every interaction triggers strategy feels fake.

## Do not reveal everything because debugging data exists

Debug UI is not player UI.

Protect the fog of social reality.

## Do not sacrifice systemic integrity for a flashy feature

If a system cannot respect time, place, knowledge, state authority, and save/load, it is not ready for the canonical trunk.

---

# 63. FEATURE ADMISSION TEST

Before adding a major feature, ask:

1. **Where does this physically happen?**
2. **How much time does it take?**
3. **Who can see or hear it?**
4. **What does the player actually know?**
5. **What do NPCs know, and how did they learn it?**
6. **Can this be interrupted?**
7. **What memories can it create?**
8. **What relationships can it affect?**
9. **What physical condition can affect it?**
10. **What opportunity is sacrificed?**
11. **What happens if the player fails?**
12. **Can an NPC perform an equivalent action?**
13. **Is there one authoritative source of truth?**
14. **Will save/load preserve it?**
15. **Does it create stories without forcing them?**

If yes, it probably belongs in CASTAWAY.

---

# 64. DIALOGUE ADMISSION TEST

Every conversation feature should answer:

- Why is this person saying this?
- Why now?
- Why to me?
- Why here?
- Who else can hear?
- What do they believe?
- What are they hiding?
- What happened recently?
- What do they want?
- What could change afterward?

If those questions cannot be answered, the dialogue is likely generic filler.

---

# 65. NPC BEHAVIOR ADMISSION TEST

When an NPC begins an activity, ask:

- What motivated it?
- Where are they now?
- Where must they travel?
- How long will it take?
- What would interrupt them?
- Who might encounter them?
- What might they learn?
- What might others infer from their absence?
- What happens when they finish?

That turns activity selection into life simulation.

---

# 66. CHALLENGE ADMISSION TEST

A new challenge should have:

- distinct interaction identity
- specific character capabilities
- meaningful player execution
- readable feedback
- touch controls
- controller controls
- mouse/keyboard where appropriate
- clean lifecycle/cleanup
- campaign integration
- NPC performance model
- save/state safety
- reasonable mobile performance

A challenge should not be included merely because it visually resembles Survivor.

It must be fun to play.

---

# 67. TRIBAL ADMISSION TEST

A Tribal feature should consider:

- current targets
- current beliefs
- idol fears
- relationships
- recent conversations
- recent betrayals
- who feels safe
- who feels excluded
- who may change
- who can whisper
- what the player knows
- what remains hidden
- what can still change before votes lock

Tribal is the compression point of the preceding social world.

---

# 68. FINAL TRIBAL ADMISSION TEST

Any FTC system must reference history.

If a juror asks:

> “Why should I respect your game?”

the answer space should come from what actually happened.

If a juror says:

> “You never protected me.”

the engine should know whether that is true, false, partially true, or a misunderstanding.

The player then decides how to respond.

---

# 69. THE IDEAL CASTAWAY MOMENT

A representative north-star moment:

It is late afternoon before Tribal.

You leave the shelter intending to find Marcus.

He is not there.

The interface says he was last seen heading toward the well.

You start walking.

Halfway there, you see Tasha returning alone.

She stops.

She looks uncomfortable.

You ask whether Marcus is at the well.

She says:

> “Yeah. He was. I don’t know where he went after.”

You can tell she is holding something back.

You decide whether to:

- press her
- pretend not to care
- tell her the rumor you heard
- ask who she is voting for
- change the subject
- keep walking

Behind you, Devon approaches.

Tasha immediately changes tone.

You realize the conversation is no longer private.

Nothing required a scripted cutscene.

It emerged because:

- people had locations
- Marcus moved
- Tasha encountered him
- she learned something
- she had a relationship with you
- she was hiding information
- Devon happened to approach
- privacy changed

**That is CASTAWAY.**

---

# 70. THE IDEAL LONG-TERM SEASON

A complete season should allow the player to look back and say:

> “I lost because I spent too much time searching and stopped maintaining my relationships.”

or:

> “I won because I noticed early that two people were always together, got close to the quieter one, and used that relationship at merge.”

or:

> “I thought she betrayed me. At FTC I found out she had actually tried to save me.”

or:

> “That challenge loss destroyed us because everyone blamed the wrong person.”

or:

> “I carried that fake idol for nine days because someone I trusted lied to me.”

These are not achievement descriptions.

They are **memories of a simulated life**.

---

# 71. NORTH-STAR SUCCESS CRITERIA

CASTAWAY is succeeding when:

1. Two campaigns with the same broad structure produce different social histories.
2. NPCs act on information the player does not possess.
3. NPCs can hold false beliefs.
4. Player beliefs can be wrong.
5. Time spent on one action creates missed opportunity elsewhere.
6. The player can infer strategy through observation rather than omniscient UI.
7. Earlier memories affect later decisions.
8. NPC behavior remains active offscreen.
9. Relationships are more complex than likes/dislikes.
10. Physical condition affects life and challenges.
11. Challenges feel playable rather than statistical.
12. Tribal outcomes have understandable causal histories.
13. FTC can reference real season events.
14. The world respects location and travel.
15. Save/load does not rewrite reality.
16. The player can fail in believable ways.
17. Ordinary camp life feels worthwhile.
18. People become recognizable through habits.
19. The same castaway can behave differently in different contexts.
20. The player regularly thinks: **“Wait. What are they doing?”**
21. The player occasionally thinks: **“Oh shit. They saw me.”**
22. The player eventually thinks: **“This feels like my Survivor season.”**

---

# 72. CANONICAL PRIORITY STACK

When two goals conflict, generally prioritize:

1. **Human believability**
2. **World-state integrity**
3. **Player agency**
4. **Incomplete-information integrity**
5. **Causal continuity**
6. **Survivor authenticity**
7. **Gameplay clarity**
8. **Tactile interaction**
9. **Presentation polish**
10. **Visual spectacle**

A gorgeous system that makes people behave impossibly is a regression.

A simpler system that creates believable human stories may be a major improvement.

---

# 73. PROJECT BOUNDARIES

CASTAWAY is related to—but distinct from—other projects.

## Survivor Expo
CASTAWAY is one major pillar within Survivor Expo.

Do not assume every Expo feature belongs inside CASTAWAY.

## Marooning TCG
Marooning is a separate card-game rules system.

Its mechanics and terminology should not silently become CASTAWAY simulation rules.

## CASTAWAY World Lab / Modeling School
This is the R&D pipeline for terrain, environment, characters, topology, rigging, and presentation.

It feeds CASTAWAY visually and spatially.

It should not overwrite core simulation laws.

## Challenge Labs
Individual challenge prototypes graduate into CASTAWAY only once they have stable gameplay, proper inputs, NPC simulation, cleanup, and campaign integration.

Lab success is not automatically trunk readiness.

---

# 74. DEVELOPMENT NORTH STAR

Every development session should ultimately move toward:

> **Eighteen believable people inhabit one Survivor season together, and the player is only one of them.**

Not the chosen one.

Not the omniscient manager.

Not the author.

A castaway.

The engine should continuously ask:

- Where is everyone?
- What are they doing?
- What do they need?
- What do they know?
- What do they believe?
- Who do they trust?
- Who scares them?
- What just happened?
- What do they remember?
- What are they planning?
- What can they physically do next?

And then the player enters that moving world.

---

# 75. FINAL NORTH-STAR STATEMENT

CASTAWAY should feel less like selecting Survivor content and more like **inhabiting a reality-TV social ecosystem**.

Its power will not come from the number of twists, dialogue lines, advantages, or minigames.

Its power will come from **causality**.

People are somewhere.

They are doing something.

They know some things and not others.

They care about some people more than others.

They make choices.

The player makes choices.

Those choices consume time.

Other things happen.

People notice.

People misunderstand.

People remember.

Plans change.

Bodies get tired.

Relationships deepen.

Trust breaks.

Votes happen.

People leave.

The remaining castaways live with what happened.

And eventually, a jury decides what the season meant.

That is the game.

> **CASTAWAY is not a Survivor story generator.  
> CASTAWAY is a Survivor world capable of producing stories.**

---

# APPENDIX A — COMPACT PROJECT INSTRUCTION

**Treat the CASTAWAY Narrative North Star Dossier as canonical product philosophy. Preserve spatial continuity, time cost, incomplete information, separate world/player/NPC knowledge, directional multidimensional relationships, persistent memory, NPC offscreen autonomy, physical possession, one authoritative state per concept, player+character skill challenge design, and emergent rather than scripted storytelling. Never make the game more omniscient, more menu-driven, more teleport-y, or more generic merely to simplify implementation. When proposing a feature, explain where it physically occurs, how long it takes, who can witness it, what information it creates, what can interrupt it, what memory/consequences it leaves, and how it interacts with save/load and authoritative simulation state.**

---

# APPENDIX B — FIVE QUESTIONS TO ASK WHEN DEVELOPMENT DRIFTS

If CASTAWAY starts feeling wrong, ask:

1. **Are these people actually living, or are they waiting for the player?**
2. **Does the player know something only because the engine knows it?**
3. **Did this action happen somewhere, take time, and have possible witnesses?**
4. **Will anybody remember this tomorrow?**
5. **Could this exact situation have emerged differently from the simulation?**

If several answers are “no,” development is drifting away from the north star.

---

**Document role:** Canonical narrative/product north star  
**Project:** CASTAWAY  
**Current development era:** Living Camp → Routine Identity → Social Gravity → Conversation 2.0  
**Intended use:** Persistent Project knowledge, feature review, design arbitration, implementation guidance, and future-agent onboarding
