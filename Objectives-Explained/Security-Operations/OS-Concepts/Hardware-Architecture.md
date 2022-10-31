# Hardware Architecture

This is a very unclear part of the objectives given how broad the topic of computer hardware architecture is; I've included only very high-level notes here since this is a security exam, not an OS exam.

## Explanation

Modern computer hardware architecture is almost universally comprised of the following components:

- CPU = central processing unit; intreprets and processes information
- memory = volatile storage used for immediate usage by CPU
- storage = non-volatile memory used for storing data beyond immediate term
- network card = network interface card, NIC; used to communicate with other devices on a network
- video display = often takes the form of a GPU which is a bunch of smaller computing devices that operate in parallel; in smaller devices it may just be a card used to process graphics
- I/O device = an device used to accept input from outside of the system
- internal bus = mechanism for connecting all internal hardware

All of these hardware components, except the CPU, rely on separate "drivers" that tell the kernel how to interact with them

## Importance

Since each of these hardware components has its own software (or firmware), they each bring with them another potential attack vector.  Hiding malware in a swapped hardware component is difficult to do, but also very difficult to detect.

## Resources

- [digipen - Overview of Operating Systems and Computer Architecture](https://azrael.digipen.edu/~mmead/www/Courses/CS180/OSOverview.html)
