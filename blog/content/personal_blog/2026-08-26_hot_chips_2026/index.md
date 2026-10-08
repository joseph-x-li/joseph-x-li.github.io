+++
title = "Hot Chips 2026 Retrospective"
draft = true
+++

I just wrapped up my first time going to Hot Chips, which ran from 2026-08-23 to 2026-08-25. 

First, I want to thank two college friends, Mason and Larry, for accompanying me to talks and answered my dumb hardware questions.  
I also am grateful to Eddie for providing a place to sleep on such short notice. 

Before the conference, I set some questions to answer so I could make the best use of my time. 
 - Figure out what is going on in the memory industry
 - Figure out to what extent the process of making a chip can be automated by AI
 - Gauge VC appetite for new semiconductor startups

## Fun Bits

I want to start with some fun highlights. The value of a conference is not just its technical talks but also the ability to congregate industry veterans, influencers, and press. And then force them to talk to me.

I met Ian Cutress ([Twitter/X](https://x.com/IanCutress)):
{{ image(path="/personal_blog/2026-08-26_hot_chips_2026/ian.jpeg") }}

I also saw Dylan Patel and was told that Jon from Asianometry was there too. I'm actually quite bummed I didn't run into Jon.

I met and chatted lots of accomplished VCs, engineers, and press who were unusually willing to exchange numbers.

#### Merch Haul

<div class="image-grid">
{{ image(path="/personal_blog/2026-08-26_hot_chips_2026/bag.jpeg") }}
{{ image(path="/personal_blog/2026-08-26_hot_chips_2026/etched.jpeg") }}
{{ image(path="/personal_blog/2026-08-26_hot_chips_2026/gcp.jpeg") }}
{{ image(path="/personal_blog/2026-08-26_hot_chips_2026/pin.jpeg") }}
</div>



## The Memory Industry: Where are we and where we are going?

TLDR: Models are not getting smaller. HBM is going nowhere. Advanced packaging will soon become table stakes for any serious accelerator.

Frontier AI is very memory hungry. Data movement is where where AI accelerators spends the majority of its energy and latency. Therefore, we should understand where memory is going if we want to understand where AI accerators are going.

There are three commercially relevant types of memory. 
 - SRAM
 - DRAM
 - Flash (NAND)

#### SRAM

#### DRAM

#### Flash (NAND)

## Is AI ready to ~~take~~ accelerate the jobs of silicon engineers?

TLDR: Probably.

When OpenAI revealed Jalapeno's development timeline and Etched revealed Sohu's development timeline, a lot of industry veterans physically standing next to me expressed incredulism. 
> "That's insane."  
> "They got rev 0 to work?"

I did not sympathize with their reactions. A lot of the semiconductor development process is verifiable, and AI models are very strong at verifiable tasks. Therefore, it should not be surprising that AI models are strong at semiconductor development.

Then it dawned on me that this might be the first time any of these (50+ year old) people have ever seen the power of Agentic AI. I think I just witnessed the hardware version of the software industry's Opus 4.5/Claude Code moment. 

In this section, I'll dive into what parts of the Hardware Development Lifecycle (HDLC) are ready to fall.


## Venture Capital: Are we out of money yet?

TLDR: No.

In fact, We are on the rising edge of a huge rotation away from traditional SaaS and into performant semiconductor tooling, design, and verification, followed by a predicted second wave of new AI hardware. 



## Extra: Advanced packaging is finally here.

## Extra: Did I go to the wrong conference?

TLDR: I fear that LLMs are taking over the narrative and we are ignoring the second wave robotics AI hardware.

Legitimately every single talk was only focused on datacenter. I cannot tell you how many times I heard the phrase "scale-out, scale-up, scale-in" ([So Lo Mo](https://www.youtube.com/watch?v=AurrFCa437g) anyone?). If this conference stays focued on datacenter, I can predict every single talk for next three years: 
 - Memory is going to get faster and denser. 
 - Everyone is going to have MX4 and FP4. 
 - Advanced packaging is going to bring down energy consumption.
 - Hardware/model co-design with a frontier AI lab will be the only way for any AI chip to be true pareto.

Ok fine. so what did I _want_ to see?

How are we investing billions of dollars in robotics and have not yet begun investing in low-latency single-batch hardware? I posed this exact question to a VC who asked me what I would invest in if I were a partner. The common answer is that this is the market for low-powered AI accelerators that can host medium-sized AI models -- and because they are low-powered, they're just not exciting to cover. 