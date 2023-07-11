Welcome to the ops102-Reading_notes wiki!
this where i'm gonna put my reading notes for the day.</br>
# Reading01</br>
This case is important to what we're doing in class today because it is a massive example of how software is not the only vulnerability in secure networks. It shows that hardware can be compromised at the manufacturing level, and that when it comes to security due dillegence needs to be done on all fronts.

### how is a hardware hack different from a software hack?
* a software hack is a hack that targets abstract features of a network, like in the case of the vtech hacker, who exploited an existing network without having to modify any physical hardware. By contrast, a hardware hack is an attack that starts by targeting physical aspects of a computer, and while the definition of this is vague, in the case of "the big hack", it refers to modification done at the manufacturing level to provide bad actors with backdoor access to critical infrastructure.</br>
### what are the two ways for spies to alter a computer's hardware?
* there is interdiction, in which the product is intercepted by the hacker as it is on its way to the consumer, the other method involves the hacker making the alterations at the manufacturing level, as was the case with China</br>
### Explain how the hack worked
* People's Liberation Army manufactured microchips that were either super tiny or disguised as other motherboard parts, which were implanted on motherboards sent to be made into servers by supermicro. They were then distributed to supermicro's clients, including Elemental, where the tiny chips changed aspects of the operating system so that it could communicate data with computers controlled by the hackers.</br>
### how did we find out?
* Amazon was thinking of acquiring Elemental inc., so a third party security service was brought in to analyze the physical server boards manufactured by the company Supermicro for Elemental. The security company discovered the tiny microchips on the motherboards, reported it to Amazon, who reported it to the US Authorities. An investigation was launched into Supermicro and the origin of the microchips, which pinpointed bad actors in China as the hack's source.</br>
## things I want to know more about:
* how do microchips work, how could this tiny piece of hardware make core modifications to the OS of the systems they're installed on. What steps are taken by companies typically to prevent occurences like this; amazon was able to hire a third party security company, but what can smaller organizations do at the manual level to prevent using compromised hardware or know if their hardware is compromised? How much information was China able to gather from US companies for how long? Does this have anything to do with the CHIPS act? how is the CHIPS act going to affect the cybersecurity field in the future? How is this hack going to affect the cybersecurity field over the coming years?
