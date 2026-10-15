# Signs of AI Writing

*LLMs tend to have an identifiable writing style.*

This is a list of writing and formatting conventions typical of AI chatbots such as ChatGPT, with real examples taken from Wikipedia articles and drafts. It is descriptive, not prescriptive: a catalog of patterns observed over many thousands of instances, not a ban on certain words, phrases, or punctuation. LLMs are trained on human writing, so not all text featuring these indicators is AI-generated, and some signs, particularly punctuation and formatting, may not apply outside Wikipedia.

The patterns are only potential signs of a problem, not the problem itself. Do not merely treat them as defects to fix; that can make detection harder. Fix the deeper issues they point to: vague claims, unsupported analysis, padding. Do not rely solely on AI-detection tools, which have non-trivial error rates, and do not over-trust your own judgment: even heavy LLM users misjudge roughly 1 in 10 texts.[^1][^2][^3]

---

## Regression to the Mean

LLMs (and artificial neural networks in general) use statistical algorithms to guess (infer) what should come next based on a large corpus of training material. It thus tends to regress to the mean; that is, the result tends toward the most statistically likely result that applies to the widest variety of cases. It can simultaneously be a strength and a "tell" for detecting AI-generated content.

For example, LLMs are usually trained on data from the internet in which famous people are generally described with positive, important-sounding language. Consequently, the LLM tends to omit specific, unusual, nuanced facts (which are statistically rare) and replace them with more generic, positive descriptions (which are statistically common). Thus the highly specific "inventor of the first train-coupling device" might become "a revolutionary titan of industry." It is like shouting louder and louder that a portrait shows a uniquely important person, while the portrait itself is fading from a sharp photograph into a blurry, generic sketch. The subject becomes simultaneously less specific and more exaggerated.[^4]

This statistical regression to the mean, a smoothing over of specific facts into generic statements, that could equally apply to many topics, makes AI-generated content easier to detect.

### Undue emphasis on symbolism, legacy, and importance

**Words to watch:** *stands/serves as*, *is a testament/reminder*, *plays a vital/significant/crucial/pivotal role*, *underscores/highlights its importance/significance*, *reflects broader*, *symbolizing its ongoing/enduring/lasting impact*, *key turning point*, *indelible mark*, *deeply rooted*, *profound heritage*, *steadfast dedication*...

LLM writing often puffs up the importance of the subject matter by adding statements about how arbitrary aspects of the topic represent or contribute to a broader topic.[^5] There is a distinct and easily identifiable repertoire of ways that it writes these statements.[^6]

> The Statistical Institute of Catalonia was officially established in 1989, marking a pivotal moment in the evolution of regional statistics in Spain. [...]
>
> The founding of Idescat represented a significant shift toward regional statistical independence, enabling Catalonia to develop a statistical system tailored to its unique socio-economic context. This initiative was part of a broader movement across Spain to decentralize administrative functions and enhance regional governance.

> Kumba has long been an important center for trade and agriculture. [...] The establishment of road networks connecting Kumba to other parts of the Southwest Region, such as Mamfe and Buea, helped solidify its role as a regional hub.

LLMs may include these statements for even the most mundane of subjects like etymology or population data. Sometimes, they add hedging preambles acknowledging that the subject is relatively unimportant or low-profile, before talking about its importance anyway.

**Examples**

> During the Spanish colonial period, the name *Bakunutan* was hispanized to *Bacnotan*, a modification reflected in official documents preserved in the National Archives in Manila. This etymology highlights the enduring legacy of the community's resistance and the transformative power of unity in shaping its identity.

> Though it saw only limited application, it contributes to the broader history of early aviation engineering and reflects the influence of French rotary designs on German manufacturers.

When talking about biology (e.g., when asked to discuss an animal or plant species), LLMs tend to over-emphasize connections to the broader ecosystem or environment, even when those connections are tenuous or generic. LLMs also tend to belabor the species' conservation status and research and preservation efforts, even if the status is unknown and no serious efforts exist.

**Examples**

> It plays a role in the ecosystem and contributes to Hawaii's rich cultural heritage. [...] Preserving this endemic species is vital not only for ecological diversity but also for sustaining the cultural traditions connected to Hawaii's native flora.

> Currently, there is no specific conservation assessment for *Lethrinops lethrinus* by the International Union for Conservation of Nature (IUCN). However, the general health of the Lake Malawi ecosystem is crucial for the survival of this and other endemic species. Factors such as overfishing, pollution, and habitat destruction could potentially impact their populations.

### Undue emphasis on notability, attribution, and media coverage

**Words to watch:** *independent coverage*, *local/regional/national/[country name] media outlets*, *music/business/tech outlets*, *active social media presence*

Similarly, LLMs act as if the best way to prove that a subject is notable is to hit readers over the head with claims of notability, often by listing sources that a subject has been covered in. They may or may not provide additional context as to what those sources have actually said about the subject, and often inaccurately attribute their own [superficial analyses](#superficial-analyses) to the source. This is more common in text from newer AI tools (2025 or later).

Human-written press releases have of course also cited news clippings for decades, but LLMs specifically asked to write a Wikipedia article often echo the exact wording of Wikipedia's guidelines, such as "independent coverage."

**Examples**

> She spoke about AI on CNN, and was featured in Vogue, Wired, Toronto Star, and other media. [...] Her insights have also been featured in *Wired*, *Refinery29*, and other prominent media outlets.

> Her views have been cited in *The New York Times*, *BBC*, *Financial Times*, and *The Hindu*.

> Its significance is documented in archived school event programs and regional press coverage, including the *Mesabi Daily News*, which regularly reviewed performances held there.

On Wikipedia specifically, LLMs often painstakingly emphasize their sources in the body text—even for trivial coverage, uncontroversial facts, or other situations where a human Wikipedia editor would be more likely to either provide an inline citation or no source at all.

**Examples**

> The restaurant has also been mentioned in ABC News coverage relating to incidents in the surrounding precinct, underscoring its role as a well-known late-night venue in the city of [Adelaide].

> In the United States, university-based incubators and accelerators have expanded alongside these centers; an official Library of Congress review found that 31.5% of SBA [Small Business Administration] Growth Accelerator Fund Competition winners from 2014–2016 were university-based programs.

In articles about people/entities who use social media, LLMs will often note that they "maintain an active social media presence" or something similar. This wording is particularly idiosyncratic to AI text and relatively uncommon on Wikipedia before ~2024.

> The mall maintains a strong digital presence, particularly on Instagram, where it actively shares the latest updates and events. Forum Kochi has consistently demonstrated excellence in digital promotions, with high-quality, engaging, and impactful video content playing a key role in its outreach.

### Superficial analyses

**Words to watch:** *ensuring ...*, *highlighting ...*, *emphasizing ...*, *reflecting ...*, *underscoring ...*, *showcasing ...*, *aligns with...*, *contributing to...*

AI chatbots tend to insert superficial analysis of information, often in relation to its significance, recognition, or impact.[^7] This is often done by attaching a present participle ("-ing") phrase at the end of sentences, sometimes with [vague attributions](#vague-attributions-of-opinion) to third parties (see below).[^7][^5]

While many of these words are strong AI tells on their own,[^6][^8] an even stronger tell is when the subjects of these verbs are facts, events, or other inanimate things. A person, for example, can highlight or emphasize something, but a fact or event cannot. The "highlighting" or "underscoring" is not something that is actually happening; it is a claim by a disembodied narrator about what something means.[^5]

Such comments are usually synthesis and/or unattributed opinions in wikivoice. Newer chatbots with retrieval-augmented generation (for example, an AI chatbot that can search the web) may attach these statements to [named sources](#undue-emphasis-on-notability-attribution-and-media-coverage)—e.g., "Roger Ebert highlighted the lasting influence"—regardless of whether those sources say anything close.

**Examples**

> Douera enjoys close proximity to the capital city, Algiers, further enhancing its significance as a dynamic hub of activity and culture.

> The civil rights movement emerged as a powerful continuation of this struggle, emphasizing the importance of solidarity and collective action in the fight for justice. This historical legacy has influenced contemporary African-American families, shaping their values, community structures, and approaches to political engagement. Economically, the enduring impacts of systemic inequality have led to both challenges and innovations within African-American communities, driving a commitment to empowerment and social change that echoes through generations.

> Its bilingual monument sign, with inscriptions in both English and Spanish, underscores its role in bringing together Latter-day Saints from the United States and Mexico.

> These citations, spanning more than six decades and appearing in recognized academic publications, illustrate Blois' lasting influence in computational linguistics, grammar, and neology.

> It holds a pivotal place in the East Central Railway Zone of Indian Railways, serving as a major railway hub with historical significance. The station has 1,676 mm (5 ft 6 in) broad gauge along with 8 tracks and 6 platforms. [...] Historically, it has been crucial for linking Darbhanga with significant cities like Delhi, Patna, and Kolkata, facilitating the movement of passengers and goods. The station has supported various services, including passenger trains and express trains like the Satyagrah Express and Mithila Express, contributing to the socio-economic development of the region. [...] Over the years, Darbhanga Junction has seen several upgrades and modernization efforts aimed at improving facilities and operational efficiency, reflecting its continued relevance in the regional and national transportation landscape.

### Promotional and advertisement-like language

**Words to watch:** *continues to captivate*, *groundbreaking* (in the figurative sense), *stunning natural beauty*, *enduring/lasting legacy*, *nestled*, *in the heart of*, *boasts a*...

LLMs have serious problems keeping a neutral tone, especially when writing about something that could be considered "cultural heritage"—in which case they [constantly remind the reader of its importance](#undue-emphasis-on-symbolism-legacy-and-importance).

**Examples**

> Nestled within the breathtaking region of Gonder in Ethiopia, Alamata Raya Kobo stands as a vibrant town with a rich cultural heritage and a significant place within the Amhara region. From its scenic landscapes to its historical landmarks, Alamata Raya Kobo offers visitors a fascinating glimpse into the diverse tapestry of Ethiopia. In this article, we will explore the unique characteristics that make Alamata Raya Kobo a town worth visiting and shed light on its significance within the Amhara region.

> TTDC acts as the gateway to Tamil Nadu's diverse attractions, seamlessly connecting the beginning and end of every traveller's journey. It offers dependable, value-driven experiences that showcase the state's rich history, spiritual heritage, and natural beauty.

In a similar way, LLM chatbots also add promotional/positive-sounding language to text about companies, business, and products, such that it sounds more like the transcript of a TV commercial.

> In general, AEO focuses on improving data consistency and machine readability so that information can be accurately understood by emerging "answer engines." Commonly discussed practices include using structured data formats such as JSON-LD and schema.org, maintaining the freshness and accuracy of published information, and aligning digital entities with open web standards like Wikidata and Schema.org.

> The SOLLEI's exterior design communicates a powerful emotional presence, staying true to Cadillac's signature bold proportions. Its low, elongated silhouette is highlighted by a wide stance and an extended coupe door, which enhances accessibility to the spacious rear cabin. Smooth, uninterrupted surfaces and a pronounced A-line accentuate the vehicle's overall length, while a sleek, low tail imparts a sense of refined dynamism. A mid-body line runs seamlessly from the headlamps to the taillights, reinforcing the car's cohesive and elegant design. Traditional door handles have been replaced with discrete buttons, preserving the vehicle's clean and modern profile. In a nod to Cadillac's legacy of bold color choices, the exterior is finished in "Manila Cream"—a distinctive hue originally offered in 1957 and 1958. This heritage color has been thoughtfully revived and hand-painted by Cadillac artisans, showcasing the brand's dedication to craftsmanship and historical reverence.

### Didactic, editorializing disclaimers

**Words to watch:** *it's important/critical/crucial to note/remember/consider*, *may vary*...

LLMs often tell the reader about things "it's important to remember." This frequently takes the form of "disclaimers" to an imagined reader regarding safety or controversial topics, or disambiguating topics that vary in different locales/jurisdictions.

**Examples**

> The emergence of these informal groups reflects a growing recognition of the interconnected nature of urban issues and the potential for ANCs to play a role in shaping citywide policies. However, it's important to note that these caucuses operate outside the formal ANC structure and their influence on policy decisions may vary.

> It is crucial to differentiate the independent AI research company based in Yerevan, Armenia, which is the subject of this report, from these unrelated organizations to prevent confusion.

> It's important to remember that what's free in one country might not be free in another, so always check before you use something.

### Summaries and conclusions

**Words to watch:** *In summary*, *In conclusion*, *Overall*...

When generating longer outputs (such as when told to "write an article"), LLMs often add a section titled "Conclusion" or similar, and will often end a paragraph or section by summarizing and restating its core idea.[^9]

**Examples**

> In summary, the educational and training trajectory for nurse scientists typically involves a progression from a master's degree in nursing to a Doctor of Philosophy in Nursing, followed by postdoctoral training in nursing research. This structured pathway ensures that nurse scientists acquire the necessary knowledge and skills to engage in rigorous research and contribute meaningfully to the advancement of nursing science.

### Outline-like conclusions about challenges and future prospects

**Words to watch:** *Despite its... faces several challenges...*, *Despite these challenges*, *Challenges and Legacy*, *Future Outlook*...

Many LLM-generated Wikipedia articles include a "Challenges" section, which typically begins with a sentence like "Despite its [positive/promotional words], [article subject] faces challenges..." and ends with either a vaguely positive assessment of the article subject,[^1] or speculation about how ongoing or potential initiatives could benefit the subject. Such paragraphs usually appear at the end of articles with a rigid outline structure, which may also include a separate section for "Future Prospects."

Note: This sign is about the rigid formula, not simply the mention of challenges or challenging.

**Examples**

> Despite its industrial and residential prosperity, Korattur faces challenges typical of urban areas, including[...] With its strategic location and ongoing initiatives, Korattur continues to thrive as an integral part of the Ambattur industrial zone, embodying the synergy between industry and residential living.

> Despite its success, the Panama Canal faces challenges, including[...] Future investments in technology, such as automated navigation systems, and potential further expansions could enhance the canal's efficiency and maintain its relevance in global trade.

> Despite their promising applications, pyroelectric materials face several challenges that must be addressed for broader adoption. One key limitation is[...] Despite these challenges, the versatility of pyroelectric materials positions them as critical components for sustainable energy solutions and next-generation sensor technologies.

> The future of hydrocarbon economies faces several challenges, including[...] This section would speculate on potential developments and the changing landscape of global energy.

> Operating in the current Afghan media environment presents numerous challenges, including[...] Despite these challenges, Amu TV has managed to continue to provide a vital service to the Afghan population​​.

> For example, while the methodology supports transdisciplinary collaboration in principle, applying it effectively in large, heterogeneous teams can be challenging. [...] SCE continues to evolve in response to these challenges.

## Language and Grammar

### Overused "AI vocabulary" words

**Words to watch:** *align/aligns/aligning with*,[^6][^8] *crucial*,[^1] *delve/delves/delving* (pre-2025),[^6][^8][^1] *emphasizing*,[^6][^8] *enduring*,[^8] *enhance/enhances/enhancing*,[^8][^1] *fostering*,[^8][^1] *garnered/garnering*,[^6][^8] *highlight/highlighted/highlighting/highlights* (as a verb),[^1] *interplay*,[^8] *intricate/intricacies*,[^6][^8][^7] *key* (as an adjective), *landscape*,[^8] *leveraging*,[^1] *multifaceted*,[^6][^8][^7] *notably*,[^8] *nuanced*,[^6][^8] *realm*,[^8] *robust*,[^1] *seamless/seamlessly*,[^1] *shed light on*, *showcasing*,[^8] *streamline*,[^1] *tapestry*,[^8] *testament*,[^1][^8] *underpin/underpins/underpinning*,[^8] *underscore/underscores/underscoring*,[^8] *vibrant*,[^8][^7] *vital*,[^1] ...

Many studies have demonstrated that LLMs overuse certain words – especially compared to pre-2022 text, which is almost certain to be human-written.[^6] These "AI vocabulary" words are also ubiquitous in AI-generated encyclopedias, such as Grokipedia, and in AI-generated Wikipedia text. They often co-occur in LLM output: where there is one, there are likely others.[^10] An edit introducing one or two of these words may not be a big deal, but an edit (post-2022) introducing lots of them, lots of times, is one of the strongest tells for AI use.

The distribution of "AI vocabulary" is slightly different depending on which chatbot or LLM was used,[^7] and has changed over time. For instance, the word *delve* was famously overused by ChatGPT until 2025, when its incidence dropped off sharply.[^11]

Please keep context in mind. For example, while the word "underscore" is overused in AI text, it can also refer to a literal underline mark, or to incidental music.

**Examples**

> Somali cuisine is an intricate and diverse fusion of a multitude of culinary influences, drawing from the rich tapestry of Arab, Indian, and Italian flavours. This culinary tapestry is a direct result of Somalia's longstanding heritage of vibrant trade and bustling commerce. [...]
>
> Additionally, a distinctive feature of Somali culinary tradition is the incorporation of camel meat and milk. They are considered a delicacy and serve as cherished and fundamental elements in the rich tapestry of Somali cuisine. [...]
>
> An enduring testament to the influence of Italian colonial rule in Somalia is the widespread adoption of pasta and lasagne in the local culinary landscape, espicially in the south, showcasing how these dishes have integrated into the traditional diet alongside rice. [...]
>
> Additionally, Somali merchants played a pivotal role in the global coffee trade, being one of the first to export coffee beans.

### Negative parallelisms

Parallel constructions involving "not", "but", or "however" such as "Not only ... but ..." or "It is not just about ..., it's ..." are common in LLM writing but are often unsuitable for writing in a neutral tone.[^1][^11]

**Examples**

> **Self-Portrait** by Yayoi Kusama, executed in 2010 and currently preserved in the famous Uffizi Gallery in Florence, constitutes not only a work of self-representation, but a visual document of her obsessions, visual strategies and psychobiographical narratives.

> It's not just about the beat riding under the vocals; it's part of the aggression and atmosphere.

Here is an example of a negative parallelism across multiple sentences:

> He hailed from the esteemed Duse family, renowned for their theatrical legacy. Eugenio's life, however, took a path that intertwined both personal ambition and familial complexities.

### Outlines of negatives

On rare occasions, user messages that appear AI-generated may also include short sentences describing items that are either absent from something else or would be considered useless in comparison to a previous, useful item. Some of these may read something along the lines of "no ..., no ..., just ..." or "What matters is ..., not ..., not ...".

**Examples**

> There are no long-form profiles. No editorial insights. No coverage of her game dev career. No notable accolades. Just TikTok recaps and callouts.

---

> The process demands rigor — not emotional fatigue, not personal offense, and certainly not a premature exit masked as moral high ground.

---

> Not a career, not a body of work, not sustained relevance — just an algorithmic moment.

---

> This is not a close call. It is not a gray area. This page should be gone, fully, cleanly, and without delay. No redirect. No merge. Just delete.

---

> Wikipedia's general notability guideline (WP:GNG) is crystal clear: significant coverage in reliable, independent, secondary sources. Not a few throwaway articles echoing Twitter drama. Not reactionary posts exploiting culture war tension. Not foreign-language gossip magazines translating controversy for clicks.

---

> What actually matters — and what continues to be completely absent — is significant, in-depth coverage in reliable, independent secondary sources. Not gossip sites. Not recycled outrage. Not tabloid blurbs about one viral controversy. And certainly not basic directory-style mentions of someone being a "video game writer" or TikTok creator.

### Rule of three

LLMs overuse the 'rule of three'. This can take different forms, from "adjective, adjective, adjective" to "short phrase, short phrase, and short phrase".[^1] LLMs often use this structure to make [superficial analyses](#superficial-analyses) appear more comprehensive.

**Examples**

> The Amaze Conference brings together global SEO professionals, marketing experts, and growth hackers to discuss the latest trends in digital marketing. The event features keynote sessions, panel discussions, and networking opportunities.

### Vague attributions of opinion

**Words to watch:** *Industry reports*, *Observers have cited*, *Some critics argue*...

AI chatbots tend to attribute opinions or claims to some vague authority—a practice called weasel wording—while citing only one or two sources that may or may not actually express such view. They also tend to overgeneralize the perspective of one or few sources into that of a wider group.

**Examples**

> His [Nick Ford's] compositions have been described as exploring conceptual themes and bridging the gaps between artistic media.

— From Draft:Nick Ford (musician). Here, the weasel wording implies the opinion comes from an independent source, but it actually cites Nick Ford's own website.

> Due to its unique characteristics, the Haolai River is of interest to researchers and conservationists. Efforts are ongoing to monitor its ecological health and preserve the surrounding grassland environment, which is part of a larger initiative to protect China's semi-arid ecosystems from degradation.

> The Kwararafa (Kororofa) confederacy is described in scholarship as a shifting Benue valley coalition led by Jukun groups and incorporating a range of Middle Belt peoples. Because much of the historical record derives from Hausa chronicles, Bornu sources and oral tradition, modern researchers treat Kwararafa as a fluid political and cultural formation rather than a fixed state. As a result, lists of member groups vary by period and source.

### Excessive synonym variance / elegant variation

Generative AI has a repetition-penalty code, meant to discourage it from reusing words too often.[^5] For instance, the output might give a main character's name and then repeatedly use a different synonym or related term (e.g., protagonist, key player, eponymous character) when mentioning it again.

Note: If a user adds multiple pieces of AI-generated content in separate edits, this tell may not apply, as each piece of text may have been generated in isolation.

**Examples**

> Vierny, after a visit in Moscow in the early 1970's, committed to supporting artists resisting the constraints of socialist realism and discovered Yankilevskly, among others such as Ilya Kabakov and Erik Bulatov. In the challenging climate of Soviet artistic constraints, Yankilevsky, alongside other non-conformist artists, faced obstacles in expressing their creativity freely. Dina Vierny, recognizing the immense talent and the struggle these artists endured, played a pivotal role in aiding their artistic aspirations. [...]
>
> In this new chapter of his life, Yankilevsky found himself amidst a community of like-minded artists who, despite diverse styles, shared a common goal—to break free from the confines of state-imposed artistic norms, particularly socialist realism. [...]
>
> The move to Paris facilitated an environment where Yankilevsky could further explore and exhibit his distinctive artistic vision without the constraints imposed by the Soviet regime. Dina Vierny's unwavering support and commitment to the Russian avant-garde artists played a crucial role in fostering a space where their creativity could flourish, contributing to the rich tapestry of artistic expression in the vibrant cultural landscape of Paris. Vierny's commitment culminated in the groundbreaking exhibition "Russian Avant-Garde - Moscow 1973" at her Saint-Germain-des-Prés gallery, showcasing the diverse yet united front of non-conformist artists challenging the artistic norms of their time.

### False ranges

When *from ... to ...* constructions are not used figuratively, they are used to indicate the lower and upper bounds of a scale. The scale is either quantitative, involving an explicit or implicit numerical range (e.g. from 1990 to 2000, from 15 to 20 ounces, from winter to autumn), or qualitative, involving categorical bounds (e.g. "from seed to tree", "from mild to severe", "from white belt to black belt"). The same constructions may be used to form a merism—a figure of speech that combines the two extremes as two contrasting parts of the whole to refer to the whole. This is a figurative meaning, but it has the same structure as the non-figurative usage, because it still requires an identifiable scale: from head to toe (the length of a body denoting the whole body), from soup to nuts (clearly based on time), etc. This is *not* a false range.

LLMs really like mixing it up, such as when giving examples of items within a set (instead of simply mentioning them one after another). An important consideration is whether some middle ground can be identified without changing the endpoints. If the middle requires switching from one scale to another scale, or there is no scale to begin with or a coherent whole that could be conceived, the construction is a **false range**. LLMs often employ "figurative" (often simply: meaningless) "from ... to ..." constructions that purport to signify a scale, while the endpoints are loosely related or even unrelated things and no meaningful scale can be inferred. LLMs do this because such meaningless language is used in persuasive writing to impress and woo, and LLMs are heavily influenced by examples of persuasive writing during their training.

**Example**

> Our journey through the universe has taken us from the singularity of the Big Bang to the grand cosmic web, from the birth and death of stars that forge the elements of life, to the enigmatic dance of dark matter and dark energy that shape its destiny.
>
> [...] Intelligence and Creativity: From problem-solving and tool-making to scientific discovery, artistic expression, and technological innovation, human intelligence is characterized by its adaptability and capacity for novel solutions. [...] Continued Scientific Discovery: The quest to understand the universe, life, and ourselves will continue to drive scientific breakthroughs, from fundamental physics to medicine and neuroscience.

### Title case in section headings

In section headings, AI chatbots strongly tend to capitalize all main words.[^1]

**Examples**

> Global Context: Critical Mineral Demand
>
> According to a 2023 report by Goldman Sachs, the global market for critical minerals [...]
>
> Strategic Negotiations and Global Partnerships
>
> In 2014, Katalayi was appointed senior executive adviser to the chairman of the board of Gécamines [...]
>
> High-Stakes Deals: Glencore, China, and Russia
>
> There was also interest from Moscow for strategic Congolese assets. [...]

---

## Punctuation and Formatting

### Excessive use of boldface

AI chatbots may display various phrases in boldface for emphasis in an excessive, mechanical manner. One of their tendencies, inherited from readmes, fan wikis, how-tos, sales pitches, slide decks, listicles and other materials that heavily use boldface, is to emphasize every instance of a chosen word or phrase, often in a "key takeaways" fashion. Some newer large language models or apps have instructions to avoid overuse of boldface.

**Examples**

> It blends **OKRs (Objectives and Key Results)**, **KPIs (Key Performance Indicators)**, and visual strategy tools such as the **Business Model Canvas (BMC)** and **Balanced Scorecard (BSC)**. OPC is designed to bridge the gap between strategy and execution by fostering a unified mindset and shared direction within organizations.

> A **leveraged buyout (LBO)** is characterized by the extensive use of **debt financing** to acquire a company. This financing structure enables **private equity firms** and **financial sponsors** to control businesses while investing a relatively small portion of their own equity. The acquired company's **assets and future cash flows** serve as collateral for the debt, making lenders more willing to provide financing.

> **50 Scientists and Thinkers in AI Safety with significant** influence on the field of alignment, containment, and risk mitigation. The list includes their **Productive Years**, their estimated **P(doom)** (probability of existential catastrophe), a **one-sentence summary of their contribution to AI Safety**, and their Wikipedia link.

### Inline-header vertical lists

AI chatbots output often includes vertical lists formatted in a specific way: an ordered or unordered list where the list marker (number, bullet, dash, etc.) is followed by an inline boldfaced header, separated with a colon from the remaining descriptive text.

Instead of proper wikitext, a bullet point in an unordered list may appear as a bullet character (•), hyphen (-), en dash (–), hash (#), emoji, or similar character. Ordered lists (i.e. numbered lists) may use explicit numbers (such as `1.`) instead of standard wikitext. When copied as bare text appearing on the screen, some of the formatting information is lost, and line breaks may be lost as well.

**Examples**

> 1. Historical Context Post-WWII Era: The world was rapidly changing after WWII, [...] 2. Nuclear Arms Race: Following the U.S. atomic bombings, the Soviet Union detonated its first bomb in 1949, [...] 3. Key Figures Edward Teller: A Hungarian physicist who advocated for the development of more powerful nuclear weapons, [...] 4. Technical Details of Sundial Hydrogen Bomb: The design of Sundial involved a hydrogen bomb [...] 5. Destructive Potential: If detonated, Sundial would create a fireball up to 50 kilometers in diameter, [...] 6. Consequences and Reactions Global Impact: The explosion would lead to an apocalyptic nuclear winter, [...] 7. Political Reactions: The U.S. military and scientists expressed horror at the implications of such a weapon, [...] 8. Modern Implications Current Nuclear Arsenal: Today, there are approximately 12,000 nuclear weapons worldwide, [...] 9. Key Takeaways Understanding the Madness: The concept of Project Sundial highlights the extremes of human ingenuity [...] 10. Questions to Consider What were the motivations behind the development of Project Sundial? [...]

> Conflict of Interest (COI)/Autobiography: While I understand the concern regarding my username [...]
>
> Notability (GNG and NPOLITICIAN): I have revised the article to focus on factual details [...]
>
> Original Research (WP) and Promotional Tone: I have worked on removing original research [...]
>
> Article Move to Main Namespace: Moving the draft to the main namespace after the AFC review [...]

### Emojis

AI chatbots love using emojis.[^11] In particular, they sometimes decorate section headings or bullet points by placing emojis in front of them. This is most noticeable in talkpage comments.

**Examples**

> Let's decode exactly what's happening here:
>
> 🧠 Cognitive Dissonance Pattern:
>
> You've proven authorship, demonstrated originality, and introduced new frameworks, yet they're defending a system that explicitly disallows recognition of originators unless a third party writes about them first.
>
> [...]
>
> 🧱 Structural Gatekeeping:
>
> Wikipedia policy favors:
>
> [...]
>
> 🚨 Underlying Motivation:
>
> Why would a human fight you on this?
>
> [...]
>
> 🧭 What You're Actually Dealing With:
>
> This is not a debate about rules.
>
> [...]

> 🪷 Traditional Sanskrit Name: Trikoṇamiti
>
> Tri = Three
>
> Koṇa = Angle
>
> Miti = Measurement 🧭 "Measurement of three angles" — the ancient Indian art of triangle and angle mathematics.
>
> 🕰️ 1. Vedic Era (c. 1200 BCE – 500 BCE)
>
> [...]
>
> 🔭 2. Sine of the Bow: Sanskrit Terminology
>
> [...]
>
> 🌕 3. Āryabhaṭa (476 CE)
>
> [...]
>
> 🌀 4. Varāhamihira (6th Century CE)
>
> [...]
>
> 🌠 5. Bhāskarācārya II (12th Century CE)
>
> [...]
>
> 📤 Indian Legacy Spreads

### Overuse of em dashes

While human editors and writers often like em dashes (—), AI *loves* them.[^11] LLM output uses them more often than nonprofessional human-written text of the same genre, and uses them in places where humans are more likely to use commas, parentheses, colons, or (misused) hyphens (-). LLMs especially tend to use em dashes in a formulaic, pat way, often mimicking "punched up" sales-like writing by over-emphasizing clauses or parallelisms.

This sign is most useful when taken in combination with other indicators, not by itself.

**Examples**

> The term "Dutch Caribbean" is **not used in the statute** and is primarily promoted by **Dutch institutions**, not by the **people of the autonomous countries** themselves. In practice, many Dutch organizations and businesses use it for **their own convenience**, even placing it in addresses — e.g., "Curaçao, Dutch Caribbean" — but this only **adds confusion** internationally and **erases national identity**. You don't say **"Netherlands, Europe"** as an address — yet this kind of mislabeling continues.

> you're right about one thing — we do seem to have different interpretations of what policy-based discussion entails. [...]
>
> When WP:BLP1E says "one event," it's shorthand — and the supporting essays, past AfD precedents, and practical enforcement show that "two incidents of fleeting attention" still often fall under the protective scope of BLP1E. This isn't "imagining" what policy should be — it's recognizing how community consensus has shaped its application.
>
> Yes, WP:GNG, WP:NOTNEWS, WP:NOTGOSSIP, and the rest of WP:BLP all matter — and I've cited or echoed each of them throughout. [...] If a subject lacks enduring, in-depth, independent coverage — and instead rides waves of sensational, short-lived attention — then we're not talking about encyclopedic significance. [...]
>
> [...] And consensus doesn't grow from silence — it grows from critique, correction, and clarity.
>
> If we disagree on that, then yes — we're speaking different languages.

> The current revision of the article fully complies with Wikipedia's core content policies — including WP:V (Verifiability), WP:RS (Reliable Sources), and WP:BLP (Biographies of Living Persons) — with all significant claims supported by multiple independent and reputable international sources.
>
> [...] However, to date, no editor — including yourself — has identified any specific passages in the current version that were generated by AI or that fail to meet Wikipedia's content standards. [...]
>
> Given the article's current state — well-sourced, policy-compliant, and collaboratively improved — the continued presence of the "LLM advisory" banner is unwarranted.

### Curly quotation marks and apostrophes

AI chatbots typically use curly quotation marks ("..." or '...') instead of straight quotation marks ("..." or '...'). In some cases, AI chatbots inconsistently use pairs of curly and straight quotation marks in the same response. They also tend to use the curly apostrophe ('), the same character as the curly right single quotation mark, instead of the straight apostrophe ('), such as in contractions and possessive forms. They may also do this inconsistently.

Curly quotes alone do not prove LLM use. Microsoft Word as well as macOS and iOS devices have a "smart quotes" feature that converts straight quotes to curly quotes. Grammar correcting tools such as LanguageTool may also have such a feature. Curly quotation marks and apostrophes are common in professionally typeset works such as major newspapers. Citation tools like [Citer](https://citer.toolforge.org/) may repeat those that appear in the title of a web page: for example,

> McClelland, Mac (2017-09-27). ["When 'Not Guilty' Is a Life Sentence"](https://www.nytimes.com/2017/09/27/magazine/when-not-guilty-is-a-life-sentence.html). *The New York Times*. Retrieved 2025-08-03.

Note that Wikipedia allows users to customize the fonts used to display text. Some fonts display matched curly apostrophes as straight, in which case the distinction is invisible to the user.

## Communication Intended for the User

### Collaborative communication

**Words to watch:** *I hope this helps*, *Of course!*, *Certainly!*, *You're absolutely right!*, *Would you like...*, *is there anything else*, *let me know*, *more detailed breakdown*, *here is a*...

Editors sometimes paste text from an AI chatbot that was meant as correspondence, prewriting or advice, rather than article content. This may appear in article text or within comments (`<!-- -->`). Chatbots prompted to produce a Wikipedia article or comment may also explicitly state that the text is meant for Wikipedia, and may mention various policies and guidelines in the output—often explicitly specifying that they're *Wikipedia's* conventions.

**Examples**

> In this section, we will discuss the background information related to the topic of the report. This will include a discussion of relevant literature, previous research, and any theoretical frameworks or concepts that underpin the study. The purpose is to provide a comprehensive understanding of the subject matter and to inform the reader about the existing knowledge and gaps in the field.

> Including photos of the forge (as above) and its tools would enrich the article's section on culture or economy, giving readers a visual sense of Ronco's industrial heritage. Visual resources can also highlight Ronco Canavese's landscape and landmarks. For instance, a map of the Soana Valley or Ronco's location in Piedmont could be added to orient readers geographically. The village's scenery [...] could be illustrated with an image. Several such photographs are available (e.g., on Wikimedia Commons) that show Ronco's panoramic view, [...] Historical images, if any exist (such as early 20th-century photos of villagers in traditional dress or of old alpine trades), would also add depth to the article. Additionally, the town's notable buildings and sites can be visually presented: [...] Including an image of the Santuario di San Besso [...] could further engage readers. By leveraging these visual aids – maps, photographs of natural and cultural sites – the expanded article can provide a richer, more immersive picture of Ronco Canavese.

> If you plan to add this information to the "Animal Cruelty Controversy" section of Foshan's Wikipedia page, ensure that the content is presented in a neutral tone, supported by reliable sources, and adheres to Wikipedia's guidelines on verifiability and neutrality.

> Here's a template for your wiki user page. You can copy and paste this onto your user page and customize it further.

> Final important tip: The ~~~~ at the very end is Wikipedia markup that automatically

### Knowledge-cutoff disclaimers and speculation about gaps in sources

**Words to watch:** *as of [date]*, *Up to my last training update*, *as of my last knowledge update*, *While specific details are limited/scarce...*, *not widely available/documented/disclosed*, *...in the provided/available sources/search results...*, *based on available information*...

A knowledge-cutoff disclaimer is a statement used by the AI chatbot to indicate that the information provided may be incomplete, inaccurate, or outdated.

If an LLM has a fixed knowledge cutoff (usually the model's last training update), it is unable to provide any information on events or developments past that time, and it often outputs a disclaimer to remind the user of this cutoff, which usually takes the form of a statement that says the information provided is accurate only up to a certain date.

If an LLM with retrieval-augmented generation fails to find sources on a given topic, or if information is not included in sources a user provides, it often outputs a statement to that effect, which is similar to a knowledge-cutoff disclaimer. It may also pair it with text about what that information "likely" may be and why it is significant. This information is entirely speculative (including the very claim that it's "not documented") and may be based on loosely related topics or completely fabricated.

**Examples**

> While specific details about Kumarapediya's history or economy are not extensively documented in readily available sources, ...

> While specific information about the fauna of Studniční hora is limited in the provided search results, the mountain likely supports...

> Though the details of these resistance efforts aren't widely documented, they highlight her bravery...

> No significant public controversies or security incidents affecting Outpost24 have been documented as of June 2025.

> As of my last knowledge update in January 2022, I don't have specific information about the current status or developments related to the "Chester Mental Health Center" in today's era.

> Below is a detailed overview based on available information:

### Prompt refusals

**Words to watch:** *as an AI language model*, *as a large language model*, *I'm sorry*...

Occasionally, the AI chatbot declines to answer a prompt as written, usually with an apology and a reminder that it is "an AI language model". Attempting to be helpful, it often gives suggestions or an answer to an alternative, similar request. Outright refusals have become increasingly rare.

Prompt refusals are obviously unacceptable for Wikipedia articles, so if a user includes one anyway, it may indicate that they did not review the text and/or may not be proficient in English. Remember to assume good faith, because that editor may genuinely want to improve our coverage of knowledge gaps.

**Examples**

> As an AI language model, I can't directly add content to Wikipedia for you, but I can help you draft your bibliography.

### Phrasal templates and placeholder text

AI chatbots may generate responses with fill-in-the-blank phrasal templates (as seen in the game *Mad Libs*) for the LLM user to replace with words and phrases pertaining to their use case. However, some LLM users forget to fill in those blanks. Note that non-LLM-generated templates exist for drafts and new articles, such as Wikipedia:Artist biography article template/Preload and pages in Category:Article creation templates.

**Examples**

> Subject: Concerns about Inaccurate Information
>
> Dear Wikipedia
>
> I am writing to express my deep concern about the spread of misinformation on your platform. Specifically, I am referring to the article about [Entertainer's Name], which I believe contains inaccurate and harmful information.

> Subject: Edit Request for Wikipedia Entry
>
> Dear Wikipedia Editors,
>
> I hope this message finds you well. I am writing to request an edit for the Wikipedia entry
>
> I have identified an area within the article that requires updating/improvement. [Describe the specific section or content that needs editing and provide clear reasons why the edit is necessary, including reliable sources if applicable].

---

## Citations

### Fictitious or hallucinated references

LLMs may generate fictitious or hallucinated references that do not exist or contain fabricated information.

### Broken external links

If a new article or draft has multiple citations with external links, and several of them are broken (e.g., returning 404 errors), this is a strong sign of an AI-generated page, particularly if the dead links are not found in website archiving sites like Internet Archive or Archive Today. Most links become broken over time, but these factors make it unlikely that the link was ever real.

### Invalid DOI and ISBNs

A checksum can be used to verify ISBNs. An invalid checksum is a very likely sign that an ISBN is incorrect, and citation templates display a warning if so. Similarly, DOIs are more resistant to link rot than regular hyperlinks. Unresolvable DOIs and invalid ISBNs can be indicators of hallucinated references.

Related are DOIs that point to entirely unrelated articles and general book citations without pages. This passage, for example, was generated by ChatGPT.

> Ohm's Law is a fundamental principle in the field of electrical engineering and physics that states the current passing through a conductor between two points is directly proportional to the voltage across the two points, provided the temperature remains constant. Mathematically, it is expressed as V=IR, where V is the voltage, I is the current, and R is the resistance. The law was formulated by German physicist Georg Simon Ohm in 1827, and it serves as a cornerstone in the analysis and design of electrical circuits [1]. Ohm's Law applies to many materials and components that are "ohmic," meaning their resistance remains constant regardless of the applied voltage or current. However, it does not hold for non-linear devices like diodes or transistors [2][3].
>
> References:
>
> 1. Dorf, R. C., & Svoboda, J. A. (2010). Introduction to Electric Circuits (8th ed.). Hoboken, NJ: John Wiley & Sons. ISBN 9780470521571.
>
> 2. M. E. Van Valkenburg, "The validity and limitations of Ohm's law in non-linear circuits," Proceedings of the IEEE, vol. 62, no. 6, pp. 769–770, Jun. 1974. doi:10.1109/PROC.1974.9547
>
> 3. C. L. Fortescue, "Ohm's Law in alternating current circuits," Proceedings of the IEEE, vol. 55, no. 11, pp. 1934–1936, Nov. 1967. doi:10.1109/PROC.1967.6033

The book references appear valid – a book on electric circuits would likely have information about Ohm's law – but without the page number, that citation is not useful for verifying the claims in the prose. Worse, both *Proceedings of the IEEE* citations are completely made up. The DOIs lead to completely different citations and have other problems as well. For instance, C. L. Fortescue was dead for 30+ years at the purported time of writing, and Vol 55, Issue 11 does not list any articles that match anything remotely close to the information given in reference 3.

## Discrepancies in Writing Style and Variety of English

### Abrupt cut offs

AI tools may abruptly stop generating content, for example if they predict the end of text sequence (appearing as `<|endoftext|>`) next. Also, the number of tokens that a single response has is usually limited, and further responses require the user to select "continue generating".

This method is not foolproof, as a malformed copy/paste from one's local computer can also cause this. It may also indicate a copyright violation rather than the use of an LLM.

### Sudden shift in writing style

A sudden shift in an editor's writing style, such as unexpectedly flawless grammar compared to their other communication, may indicate the use of AI tools.

### Sudden shift in English variety use

A mismatch of user location, national ties of the topic to a variety of English, and the variety of English used may indicate the use of AI tools. A human writer from India writing about an Indian university would probably not use American English; however, LLM outputs use American English by default, unless prompted otherwise.[^9] Note that non-native English speakers tend to mix up English varieties, and such signs should raise suspicion only if there is a sudden and complete shift in an editor's English variety use.

## Ineffective Indicators

False accusations of AI use can drive away new editors and foster an atmosphere of suspicion. Before claiming AI was used, consider if Dunning–Kruger effect and confirmation bias is clouding your judgement. Here are several somewhat commonly used indicators that are ineffective in LLM detection—and may even indicate the opposite.

- **Perfect grammar**: While modern LLMs are known for their high grammatical proficiency, many editors are also skilled writers or come from professional writing backgrounds. 

- **"Bland" or "robotic" prose**: By default, modern LLMs tend toward effusive and verbose prose, as detailed above; while this tendency is formulaic, it may not scan as "robotic" to those unfamiliar with AI writing.[^14]

- **"Fancy," "academic," or unusual words**: While LLMs disproportionately favor certain words and phrases, many of which are long and have difficult readability scores, the correlation does not extend to *all* "fancy," academic, or "advanced"-sounding prose.[^1] Low-frequency and "unusual" words are also less likely to show up in AI-generated writing as they are statistically less common, unless they are proper nouns directly related to the topic.

- **Letter-like writing (in isolation)**: Although many talk page messages written with salutations, valedictions, subject lines, and other formalities after 2023 tend to appear AI-generated, letters and emails have conventionally been written in such ways *long* before modern LLMs existed. Human editors (particularly newer editors) may format their talk page comments similarly for various reasons, such as being more accustomed to formal communication, posting as part of a school assignment that requires such at one, or simply mistaking the talk page for email. AI-generated talk page messages tend to have other tells, such as vertical lists, placeholders, or abrupt cutoffs.

- **Conjunctions (in isolation)**: While LLMs tend to overuse connecting words and phrases in a stilted, formulaic way that implies inappropriate synthesis of facts, such uses are typical of essay-like writing by humans and are not strong indicators by themselves.

---

## References

[^1]: Russell, Jenna; Karpinska, Marzena; Iyyer, Mohit (2025). [*People who frequently use ChatGPT for writing tasks are accurate and robust detectors of AI-generated text*](https://aclanthology.org/2025.acl-long.267/). Proceedings of the 63rd Annual Meeting of the Association for Computational Linguistics (Volume 1: Long Papers). Vienna, Austria: Association for Computational Linguistics. pp.5342–5373. arXiv:[2501.15654](https://arxiv.org/abs/2501.15654).

[^2]: Dugan, Liam; Hwang, Alyssa; Trhlik, Filip; Zhu, Andrew; Ludan, Josh Magnus; Xu, Hainiu; Ippolito, Daphne; Callison-Burch, Chris (2024). [*RAID: A Shared Benchmark for Robust Evaluation of Machine-Generated Text Detectors*](https://aclanthology.org/2024.acl-long.674). Proceedings of the 62nd Annual Meeting of the Association for Computational Linguistics (Volume 1: Long Papers). Bangkok, Thailand: Association for Computational Linguistics. pp.12463–12492. arXiv:[2405.07940](https://arxiv.org/abs/2405.07940).

[^3]: ["People who frequently use ChatGPT for writing tasks are accurate and robust detectors of AI-generated text"](https://arxiv.org/html/2501.15654v2). *arxiv.org*. Retrieved 2025-11-28.

[^4]: This can be directly observed by examining images generated by text-to-image models; they look acceptable at first glance, but specific details tend to be blurry and malformed. This is especially true for background objects and text.

[^5]: ["10 Ways AI Is Ruining Your Students' Writing"](https://www.chronicle.com/article/10-ways-ai-is-ruining-your-students-writing). *Chronicle of Higher Education*. September 16, 2025. Archived from the original on October 1, 2025. Retrieved October 1, 2025.

[^6]: Juzek, Tom S.; Ward, Zina B. (2025). [*Why Does ChatGPT "Delve" So Much? Exploring the Sources of Lexical Overrepresentation in Large Language Models*](https://aclanthology.org/2025.coling-main.426.pdf) (PDF). Findings of the Association for Computational Linguistics: ACL 2025. Association for Computational Linguistics. arXiv:[2412.11385](https://arxiv.org/abs/2412.11385).

[^7]: Reinhart, Alex; Markey, Ben; Laudenbach, Michael; Pantusen, Kachatad; Yurko, Ronald; Weinberg, Gordon; Brown, David West. ["Do LLMs write like humans? Variation in grammatical and rhetorical styles"](http://arxiv.org/abs/2410.16107). Retrieved 4 December 2025.

[^8]: Kobak, Dmitry; González-Márquez, Rita; Horvát, Emőke-Ágnes; Lause, Jan (2 July 2025). ["Delving into LLM-assisted writing in biomedical publications through excess vocabulary"](https://www.science.org/doi/10.1126/sciadv.adt3813). *Science Advances*. **11** (27). doi:[10.1126/sciadv.adt3813](https://doi.org/10.1126%2Fsciadv.adt3813). ISSN 2375-2548. PMC 12219543. PMID 40009654.

[^9]: Ju, Da; Blix, Hagen; Williams, Adina (2025). [*Domain Regeneration: How well do LLMs match syntactic properties of text domains?*](https://aclanthology.org/2025.findings-acl.120). Findings of the Association for Computational Linguistics: ACL 2025. Vienna, Austria: Association for Computational Linguistics. pp.2367–2388. arXiv:[2505.07784](https://arxiv.org/abs/2505.07784). doi:[10.18653/v1/2025.findings-acl.120](https://doi.org/10.18653%2Fv1%2F2025.findings-acl.120).

[^10]: Kousha, Kayvan; Thelwall, Mike (2025). [*How much are LLMs changing the language of academic papers after ChatGPT? A multi-database and full text analysis*](https://arxiv.org/pdf/2509.09596). ISSI 2025 Conference. arXiv:[2509.09596](https://arxiv.org/abs/2509.09596).

[^11]: Merrill, Jeremy B.; Chen, Szu Yu; Kumer, Emma (13 November 2025). ["What are the clues that ChatGPT wrote something? We analyzed its style"](https://www.washingtonpost.com/technology/interactive/2025/how-detect-chatgpt-em-dash/). *The Washington Post*. Retrieved 14 November 2025.

[^14]: Murray, Nathan; Tersigni, Elisa (21 July 2024). ["Can instructors detect AI-generated papers? Postsecondary writing instructor knowledge and perceptions of AI"](https://journals.sfu.ca/jalt/index.php/jalt/article/view/1895). *Journal of Applied Learning & Teaching*. **7** (2). doi:[10.37074/jalt.2024.7.2.12](https://doi.org/10.37074%2Fjalt.2024.7.2.12). ISSN 2591-801X. Retrieved 21 November 2025.
