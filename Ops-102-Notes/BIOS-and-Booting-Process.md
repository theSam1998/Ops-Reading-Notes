# BIOS and Booting Process
---
## What is the BIOS?</br>
- The BIOS (Basic Input Output System) is responsible for ensuring power is being sent in the correct amounts to the correct places (running POST diagnostics), and locating/booting the operating system onto your PC. The OS is loaded into the RAM, and can then be used as an interface between the user and the hardware in the PC, translating visible actions in the GUI into data that can be understood by the CPU.
## Use analogies from your previous background to explain what happens during the booting process?</br>
- Compared to my background in fishing, the booting process most closely resembles the process of taking a guided trip. On a guided trip, there is often money and reputation at stake for the guide in question. The guide will have to, according to the current runs, select the proper body of water, and the proper section of that water body, as well as the right lures, rods and reels to get you into some trophy fish. In this example, the guide is akin to the bios, with the water being the operating system, the lures being the actions one would take within the user interface, and the fish are like the proper response to all of these factors coming together in harmony to create an excellent experience, or in this case, a functional PC. This example operates on the presumption that without the presence of the guide, one would not be able to interact with the water or the fish within at all.

## What is the “Power On Self Test”?</br>
- The POST is meant to check that power is being diverted in the correct places in the correct quantities. It ensures that there are no errors occuring within the hardware of the PC, before even attempting to run software. If POST fails, it means something is likely wrong or misplaced within the internals of the PC, and the hardware will indicate this either with flashing lights, beeping, or both. The order of these signals is important, as they are tied to codes that indicate what the error may be.
## What is the CMOS? </br>
- The CMOS (Complementary Metal Oxide Superconductor, what a mouthful!) is used to create integrated circuits, which are basically just smaller, more discrete versions of larger circuits meant to function as part of a greater system. In this case, the CMOS is a type of circuit that houses the BIOS data. The CMOS is like a tiny brain specifically for booting up the Operating system.

## What is the CMOS battery? </br>
- The CMOS battery provides power to the CMOS, allowing it to store volatile data such as date and time. Removing the CMOS battery will reset all this volatile data, leading to a factory reset. The CMOS also stores BIOS data, and so a dead CMOS battery can lead to the OS failing to be located by the BIOS, but can also lead to more severe problems such as hardware failure (according to https://www.learncomputerscienceonline.com/bios/)

## Things I want to know more about
- how does the GUI within the BIOS operate? Mine allows full use of the mouse and clickable windows/expanding tabs, it is quite advanced within itself.
- What data stored within the CMOS is permanent, and will remain on the CMOS regardless of the presence of the battery? Why is this data permanent while other data is ignored?
- I would like an overall greater understanding of this aspect of the PC, as I still do not entirely understand all of the BIOS's functions, the CMOS's composition, or how these parts interact with the other pieces on the motherboard.
