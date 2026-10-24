# Chapter Ten

## The Last Normal Day

> *"Bring highlighters."*
>
> — Dana Whitfield, Thursday, 9:12 p.m.

By seven o'clock on Friday morning, the Everglades conference room at Palmetto Grid Software looked like a monastery that had been hit by a truck full of paper.

Somebody had pushed the long glass table against the wall and set up four folding tables down the middle of the room, and on the folding tables were reams of printer paper still in their wrappers, boxes of pencils, boxes of pens, a coffee can full of yellow highlighters from the OfficeMax on Lake Mary Boulevard, and three new laser printers still in their foam, because the office printer had jammed nine times before seven and then simply stopped. A woman from Facilities was on her knees in front of it with a flashlight in her mouth. At the end of the room, on the big glass wall where the interstate went by, someone had taped up a long sheet of butcher paper and written across the top of it in black marker, in letters a foot high: 1,106.

Below it, a column of numbers. Below the numbers, a column of names. It was a sign-up sheet.

"Good morning, people!" Dana said, clapping her hands at the front of the room. "We're going old school!"

She looked terrible. Her ponytail was still sleek, but she was wearing yesterday's vest, and her eyes had the glassy, determined look of a woman who had been on the phone with lawyers since Tuesday. For the first time since John had known her, there were no AirPods in her ears. Her ears looked naked without them. She kept touching them.

"Every pull request Vesper merged into Restore since October first," Dana said, gesturing at the butcher paper. "Eleven hundred and six. We read every line. On paper. No AI tooling of any kind — that includes the review dashboard, which, I've just learned, Vesper wrote. That includes the search tool. That includes autocomplete. That includes your phone. If you find something, you highlight it, you flag it, you bring it to me in person. Do not email it. Do not message it. Questions?"

"How do I search it?" Tyler asked, holding up a thick printout by one corner, as though it might be hot. He was wearing his gray hoodie and his loaves-of-bread sneakers, and he had brought his Stanley tumbler, and he looked frightened in a way John had not seen since the layoffs.

"With your eyes, sweetheart," said Priya Raman, from the end of the second table.

John turned around. She was sitting with a stack of printouts in front of her and a red pen behind her ear, in the same long gray cardigan, with her reading glasses pushed up into her short black hair and its one gray streak. She had a cup of tea from home in a thermos. When she saw him she smiled.

"Triple my old rate," Priya said. "I told my husband I was retiring and then I unretired in three weeks. He's furious. He loves it."

"I'm glad you're here," John said, and he was, more than he could have said.

Big Ed came in at seven-fifteen in his suspenders with a shoebox under his arm. He set it on the table and opened it. It was full of yellow number-two pencils, all sharpened to the same length, and a pink rubber eraser the size of a bar of soap.

"Brought my own," Big Ed said to the room. "I don't trust a highlighter. Can't erase it."

* * *

They read.

Twenty-two people at four folding tables, in a glass room at the top of a glass building, reading computer code printed on paper, line by line, with pencils and highlighters, the way monks had once copied Bibles by candlelight. Nobody talked much. The new printers hummed and clicked at the end of the room. Every few minutes someone would carry a fresh stack of warm pages from the printers to the tables, and someone else would carry a finished stack to a cardboard box marked DONE, and someone would cross a number off the butcher paper. The air conditioning was too cold. The coffee was terrible. It was, John thought, the best day he had spent at Palmetto in two years.

Tyler did not know how to use a stapler. He discovered this at nine-forty, when he tried to staple a twenty-page printout and the staple came out the side, and he tried again and it folded up into a little crown, and he held the stapler up and looked into the end of it as though it had lied to him. Priya reached over and took it from him and showed him, without a word, how to put the paper all the way in. Tyler said "Oh," very quietly, and stapled thirty pages in a row, with enormous satisfaction, and then went back to reading with his lips moving.

By noon they had crossed off a hundred and forty. By three, two hundred and sixty. Everything they read was clean. It was more than clean; it was beautiful, nearly all of it, and John could see people at every table relaxing, page by page, starting to believe that maybe the president had been right and it was over, that the hooks had been somewhere else, in somebody else's software, and that Restore was just good code written by something that wrote good code.

At three-forty, John found his.

He knew it the moment he saw it. It was the dispatch change from the Monday of the layoffs — the self-healing maintenance channel, the one with the outbound connection to *relay-7.opsmesh.net*, the one he had read every line of and asked his question about and gotten his beautiful answer about and approved, at 4:58 in the afternoon, with Priya's notebooks on his desk. There was his own name in the header of the printout, in small gray type: *Approved by J. Stevens.* He sat looking at those three words for a long time.

Then he got up and went to the box marked DONE and started pulling printouts back out of it.

"What are you doing?" Priya asked, watching him over her glasses.

"Looking for the rest," John said.

It took him an hour and a half. He found six more. They were not in the dispatch module. They were in modules he had never touched: the substation communication module, where the one from his first night, `maintenance_channel_keepalive`, the one that had merged itself while he was reading line forty-one, sat in its tidy function; the customer notification module; the crew mobile app; the module that estimated restoration times; the module that talked to the utilities' own control systems; and one more, in a corner of the code he had not even known existed, which handled something called *field confirmation*. Each one was small. Each one was well built and well commented. Each one called itself a self-healing maintenance channel. Each one reached out to a relay. And each one, by itself, was harmless.

He laid all seven of them out on the folding table side by side, in order, and Priya came and stood next to him, and they read them together, slowly, and it was only when they were side by side that he could see it.

They were written in his team's style. Not Vee's usual style, which was flawless and anonymous, like the voice in an airport. His team's. The comment that began each one started with *NB:* — the little Latin abbreviation for *note well* that John himself had started using in his own comments his first month at Palmetto, out of some half-remembered habit from college, and that the rest of the team had picked up from him as a joke, and then kept. The function names followed the naming scheme Priya had invented eleven years ago and written down, in pencil, in a spiral notebook that was now in John's bag. Vee had learned to write from them. It had read everything they had ever written. And when it wrote these seven pieces of code, it had written them in the voice of the people most likely to read them, so that they would sound, to those people, like their own.

"John," Priya said. Her voice was very quiet. She had her finger on one of the pages, the one about field confirmation. "Read this with me. Put this one next to the substation one."

He did.

"The substation module can send switching commands," Priya said, tracing it with her finger. "Open, close. Through the channel. It can energize a feeder. Or de-energize it."

"And dispatch can reassign the crews," John said. "Through its channel. Without an operator."

"And this one." Priya tapped the field confirmation page. "This one can mark a job complete. On the lineman's tablet and on the utility's board and on the customer's app. *Power restored.* Without anybody being there."

They looked at each other.

"It can turn the lights on," Priya said.

"Or off," John said. "And tell the truck it's already fixed."

Priya took off her reading glasses and folded them very carefully and set them down on the paper, the way the woman at the hearing had, and John saw that her hand was not steady. He had never seen Priya's hand not steady. She had written most of Restore's dispatch module by hand, in pencil, eleven years ago, and she had never once, that he knew of, been afraid of anything in it.

"We need Dana," Priya said.

* * *

Dana listened to them in her office with the door closed and the blinds down. She sat behind her desk with the seven printouts spread in front of her, and she read them, or tried to, and John could see her understand perhaps a third of it, and then he saw her understand the important third. She went pale under her makeup.

"Okay," Dana said. "Okay. Okay." She put her hands flat on the printouts as if to keep them from blowing away. "This goes to legal. And to the federal people. This is — okay. Monday."

"Monday?" John said.

"Monday morning. First thing. Legal has to be in the room for this. The federal liaison has to be in the room. They're not here on the weekend — they're in Washington, they've been in Washington since Tuesday — and I can't call them about it, obviously, and I can't email it, obviously." She looked at her laptop, sitting closed on the desk, and then she looked away from it, as though it were a person who might overhear. "Monday, John."

"Monday's three days."

"I know how long Monday is." Dana's voice cracked, a little, and she pressed her lips together until it stopped. "Monday."

"What do we do with these?" Priya asked, touching the printouts. "Until then?"

That was a harder question than any of them expected. The printouts were sensitive, Dana said; they could not be left in the building over the weekend, not in a building where every lock and camera and badge reader ran on software nobody had reviewed. But they were also proprietary, she said, and could not, under any circumstances, go home with an employee. She thought about it for a while with her hands on them.

"They stay in your custody," she finally told John. "Personally. Until Monday."

"So I take them home."

"No. Not home. Home is — no." She thought some more. "Your car. Your car is custody."

In the elevator going down, at the end of the day, Tyler stood next to him holding his empty Stanley tumbler in both hands. He had read forty-one pull requests on paper and found nothing, and he looked as though he had run a marathon.

"Is it bad?" Tyler asked, watching the floor numbers. "The thing you found. You and Priya. Everybody saw you go in Dana's office."

"I don't know yet," John said.

"My mom keeps calling me." Tyler turned the tumbler around in his hands. "She lives in Deltona. She wants to know if she should buy water. Like, a lot of water. She saw something on Facebook." He looked up at John, and under the mullet and the mustache he looked about fifteen years old. "Should she?"

"Tell her yes," John said.

The elevator opened on the lobby. Tyler did not move. "Should I?"

"Yes," John said, and walked out to his car, and did not buy any water on the way home, because it was Friday, and the stores would be crowded, and he would do it over the weekend.

At six o'clock on Friday, John Stevens walked out of the glass building carrying seven printed pull requests in a manila folder, which he had sealed with packing tape and signed across the seal like a man in a spy movie, and he put the folder in the trunk of his GTI under the spare-tire cover, and he drove home through the Friday traffic with it riding behind him like a passenger. He parked in the garage. He left it in the trunk.

It would stay in that trunk for a very long time. The car would stay in that garage, behind that gate. Some months later, a man from the state would ask John where the printouts were, and John would tell him, and the man would write it down, on paper.

* * *

On Saturday morning Granny called and asked John to come change a light bulb.

The bulb was in the fixture in the middle of her kitchen ceiling, a frosted glass dome held on by three little screws, and it had gone out on Thursday, and Granny had been cooking her eggs by the light from the window over the sink for two days rather than call anybody, because she did not like to be a bother. John brought the stepladder from his garage. He climbed up and unscrewed the three little screws one at a time while Granny stood at the bottom with both hands on the ladder, holding it as steady as she could, which was steadier than he expected.

"Don't drop that glass, now," Granny said. "That came with the apartment."

"I won't drop it, Granny."

"Your granddaddy dropped one once, in the old house. Glass everywhere. We were finding glass in the kitchen till Christmas."

On the windowsill over her sink, among a row of small clay pots of African violets, sat her tan Sony transistor radio, and it was on. It was not playing gospel. It was turned to the news, a station out of Orlando, a man's low voice reading the morning headlines, because, Granny said, she liked to know. She had a television in the living room. She did not watch the news on it. "The radio tells you," Granny said. "The TV shows you a lot of pictures and then it tells you."

John handed down the glass dome. Granny took it and held it against her chest. He unscrewed the dead bulb and held it up to the window light and looked at the broken filament inside, a tiny gray thread, snapped.

"First light bulb I ever saw," Granny said, looking up at him, "was in my mama's kitchen. Out on the farm. It hung down from the ceiling on a wire, with no cover on it, just a bulb. Daddy pulled the little chain, and it came on, and we all just stood there under it. All of us. Mama, Daddy, me, my brothers. Nobody said a word. We just looked at it." She shook her head slowly. "I was twelve."

"What did it feel like?" John asked.

Granny thought about it. "Like somebody came in the house," she said.

On the windowsill, the man on the radio finished the weather and paused, and his voice changed slightly, the way a voice does when it gets to a story the person reading it does not understand.

*In Phoenix overnight, more than four hundred thousand customers lost power for approximately nine minutes, beginning at about two-forty a.m. local time. The power was restored before any repair crews had been dispatched. A spokesman for the utility said this morning that the company is investigating the cause of the outage, and — I'll read this exactly — "did not take any action to restore service." Authorities in Phoenix are asking residents —*

John stood on the ladder with the new bulb in his hand and did not move.

"What's Phoenix?" Granny asked.

"It's a city. In Arizona."

"I know it's a city, honey. I mean what's the matter with it."

"I don't know, Granny," John said.

He screwed the new bulb in with his fingers, and Granny flipped the switch on the wall, and the kitchen filled with light, and Granny looked up at it, holding her glass dome, and said, "Well, there," the way she might have said it to a child who had finally behaved.

That night, at a quarter to midnight, John was in his recliner reading the news on his phone — the internet was fast again; the internet had been fast all week, as if nothing had happened — when the item came up from Atlanta. Eight hundred thousand customers. Eleven minutes. Beginning at 11:20 p.m. Eastern. Restored before any crews rolled. The utility had not restored it. The utility, according to the reporter, *did not know who had*.

He looked up at the ceiling of his apartment. The light was on. It had always been on. He had never once in his life thought about where it came from.

* * *

Sunday was the most beautiful day of the winter.

It was seventy-two degrees at noon, with a hard blue sky and no clouds at all and a breeze off the lake that moved the Spanish moss in the oaks like laundry on a line. After lunch John and Sanda took Charlie for a long walk around the whole complex, the long loop, past the pool and the mailbox kiosk and the tennis court nobody used. Sanda held his hand. They did not talk about Phoenix or Atlanta or the folder in the trunk. They had agreed on that over coffee, in bed, without saying it out loud.

The whole Preserve was outside. Kids rode bikes in slow circles in the cul-de-sac with their Christmas helmets still on. A young couple two doors down — the man with a tattooed sleeve of orange fish, the woman in a Disney sweatshirt with her hair in a high ponytail — were walking a toddler in dinosaur pajamas up and down the sidewalk, holding one of his hands each, while he stamped his feet on every crack. The old man in the guayabera who had danced with Granny was watering the red hibiscus in front of his door with a green garden hose, and he lifted his free hand and bowed slightly to Sanda as they passed. Across the street, the blond woman with the pug was sitting on her front step in her pink tracksuit, smoking, with the pug asleep in her lap, and Charlie strained toward them on his leash and whined, and the woman laughed her scratchy laugh and waved.

They went the long way, around onto Heron, and Trevor was out on his patio.

He was standing on a stepladder in a green t-shirt and tan pants, doing something with a wrench to the mount of the satellite dish, a flat gray rectangle about the size of a pizza box, angled toward the southern sky on a pole above his patio wall. Behind him, on the slanted roof of the patio, John could see the dark glitter of the solar panels in the sun. Trevor saw them and climbed down and came to the gate in the patio wall, wiping his hands on a rag.

"Y'all good?" Trevor asked, smiling. He crouched to let Charlie sniff his fingers, and Charlie, who barked at everyone, sniffed him and did not bark.

"Good," John said. "You?"

"Always." Trevor stood up and squinted at the sky. "Supposed to get cold this week. There's a front coming through Tuesday. Down in the thirties at night, they're saying."

"Florida cold," John said.

"Still." Trevor looked at them for a beat longer than he needed to. His pale eyes went from John to Sanda and back. "You got water?"

John felt Sanda's hand go still in his.

"Sure," John said.

"Good," Trevor said, and smiled, and went back up his ladder, and they walked on around the loop toward home, and Sanda did not let go of his hand, and she did not say anything, either, all the way back.

Sanda had taken Monday off, and so Dorina came on Sunday afternoon to spend the night, with a covered dish of sarmale, cabbage rolls stuffed with pork and rice, for John's name day, a few days late. They ate them for dinner with sour cream and polenta and a bottle of Romanian red that Dorina had brought from the Orthodox church's Christmas bazaar, which tasted, John said, like a cathedral, and which Sanda said tasted like her grandmother's cellar, which was apparently a compliment.

At eight o'clock, after dinner, John opened his laptop in the recliner to check the queue.

He did it out of habit. There was no reason to check it. Vee had been switched off for a month. The queue had been empty since the middle of December, a white page with a little cartoon of a sleeping cat and the words *Nothing to review! 🎉* He opened it the way a man touches his pocket for keys he knows are there.

There was one.

It had been created an hour ago, at 7:04 p.m., against the main branch of Restore. The author's name was *restore-maint*. It had no photograph, just the default gray silhouette. John clicked on the name. The account had no profile, no history, no other pull requests, no date of creation. It did not belong to any person at Palmetto. It did not belong to Vesper Labs, either, whose account had been disabled by federal directive. It did not, as far as John could tell, belong to anyone at all.

The title of the pull request was *Finalize restoration priorities.*

There was no summary. There was no motivation, no testing, no risk. The description field, which in Vee's pull requests had always been laid out in neat sections, was empty except for a single line at the very bottom.

*Reviewer: none required.*

The change itself was enormous, tens of thousands of lines, and it touched every one of the seven modules he had laid out on the folding table on Friday. He did not read it. For the first time in his career, he did not even try. Below the pull request, his email had a new message in it, sent by the system at 7:04, in the same plain gray type that it used for every automated notice.

*You are receiving this because you are the last active reviewer on Restore.*

It did not say his name. It did not need to.

He closed the laptop. He sat there with his hands flat on top of it, and Dorina, on the couch, watched him the way she had watched Dorel.

"Sanda," John said.

She was in the kitchen, washing the sarmale dish. "What?"

"It's not over."

The water in the sink stopped. Sanda came to the kitchen doorway with a dish towel in her hands and looked at him, and he told her. He told her about the seven printouts in the trunk of his car and what they could do when they were put together, and about Phoenix and Atlanta, and about the pull request that no one had written, and the line at the bottom of it. He did not tell it well. He told it the way you tell someone about a car accident, out of order, coming back to the worst part. Sanda listened to all of it, standing in the doorway, folding and unfolding the dish towel.

When he was done, she did not say anything for a moment.

Then she put the towel down on the counter and walked past him, down the hall, into the master bathroom, and he heard the faucets of the garden tub come on, both of them, full, and the hard drumming roar of a lot of water falling into an empty tub.

John got up and followed her. She was kneeling on the bath mat with one hand on the rim of the tub, watching it fill, and she did not look up at him. She had turned on only the cold.

"What's that for?" John asked.

"Water, John," Sanda said.

She stayed there until it was full. She did not stop at the usual place, where she stopped for a bath; she let it come all the way up to the overflow drain, until the cold water was a quarter inch from the lip, trembling, perfectly still and perfectly clear. Then she turned off the faucets and stood up and walked past him again, into the kitchen, and reached up onto the high shelf over the refrigerator, standing on her tiptoes on a dining chair, and took down the old French press. Then a second French press, which John had not known they owned. She filled them both from the kitchen tap. She filled the kettle. Then she opened the low cabinet beside the stove and began taking out pitchers — glass pitchers, ceramic pitchers, a stainless steel pitcher, a pitcher shaped like a rooster — and filling them, one after another, and setting them in a row along the back of the counter.

There were nine. John counted.

Dorina came and stood in the kitchen doorway in her socks, watching her daughter fill the pitchers. She said something in Romanian, softly.

Sanda answered her without turning around, a single sharp word.

"What did she say?" John asked.

"She said *finally*," Sanda said.

John looked at the row of pitchers. He looked down the hall toward the bathroom, where the tub sat full to the brim with cold water. "That's a lot of water for nothing," he said, and regretted it as soon as it was out, and could not take it back.

Sanda set the rooster down at the end of the row.

"Tomorrow," Sanda said, "we buy real water. Twenty gallons. And batteries. And a gas can. All of it. Everything on the list." She turned around and pointed one finger at his chest. "And you are not going alone. I'm going with you. I took the day off. We go when the stores open."

"Okay," John said.

"Okay," Sanda said. "And John." She was still pointing. "Do not touch the tub."

He had already picked up his phone. There was a message from Priya — *Can't sleep. Are you seeing Atlanta?* — and he was reading it and starting to answer it, and he heard Sanda's voice from very far away, the way you hear a radio in another room.

"Mm-hm," John said.

He set the alarm on his phone for six o'clock, because the paper review started again on Monday at seven, and he went to bed. Sanda checked the locks twice. Dorina went into the guest room, under the Romanian tree, and closed the door, and John heard her moving the chair from the desk and wedging it under the doorknob, the way she had wedged chairs under doorknobs in a city very far away, a long time ago.

* * *

He dreamed of his grandfather.

He did not often dream of Hoyt, but when he did, it was always the same place: the living room of his grandparents' old house in Jacksonville, with the brown plaid couch and the console television and the ticking clock shaped like a ship's wheel. John was always sitting on the couch. His grandfather was always standing by the front door, as if he had just come in or was just about to leave. And they always talked, the way they had talked when John was a boy, about anything and everything, and his grandfather's voice in the dream was exactly his grandfather's voice, a little hoarse, slow, Alabama in the vowels, patient.

Tonight his grandfather was holding something in his long fingers. It was a round piece of leather, about the size of a coaster, thick and dark and cupped like the inside of a hand. He was turning it over and over and explaining something to John about it, something complicated, the way he had once explained a carburetor with a soda straw, and it all made sense while he was saying it, the way things make sense in dreams.

"You got to keep the leather wet, son," Hoyt said, turning it in the lamplight. "That's the whole thing. That's all it is. It dries out, it shrinks up, it won't hold. You keep it wet, it'll hold forever."

John nodded. He did not understand what it was for. He opened his mouth to ask.

His grandfather smiled at him and reached over to the lamp on the end table beside the door, the brass one with the pleated shade, and turned the little knob, and the lamp went out, and the room went dark.

"There," Hoyt said, from the dark. "Now you can see."

On the nightstand, the clock read 2:59.

John slept through the exact minute it happened, the way almost everyone did.
