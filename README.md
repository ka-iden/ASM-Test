# ASM-Test

Using this repo to learn my way around (x86 ftw) assembly, specifically in Systems Engineering.

>[!CAUTION]
> I have given up on this specific project, and thus far it will be archived.  
> I will not be updating it further, and any further assembly code I write may be found [here](https://github.com/ka-iden/hyperOS).

## Progress & Learning

Latest progress: Clean looking boot, refactored print, with a new hex print function!  
Latest thing I learned: How to use macros, and using the stack.  
Previous milestones:

- Clean looking boot, refactored print, with a new hex print function! (Hey! That's this milestone!)
- Abstraction of functions, print is now a seperate file!
- Bootloader that prints Hello, World!
- Bootloader that boots into Text mode!

An image from my latest milestone:  
![Bootloader that prints Hello, World!](image.png)

## Abandon Hope All Ye Who Enter Here

Assembly, especially for operating systems and systems eng. usually is looked down upon for beginners.  
But alas, I, a beginner in ASM, am taking on this boring but fulfilling challenge. (emphasis on challenge!)  
I think that setting a big, **big** project to complete over many months/years is a great idea, as long as you have other similar projects to bounce off of, so why not learn how to make an operating system at the same time as I learn how to program in ASM? I don't plan on becoming the next Linus Torvalds, but I do plan on learning a lot of assembly from this.

## Software I'm using

I'm using [NASM][nasm] to compile my assembly code.  
I'm using [QEMU][qemu] to run/emulate my code.

## Building & Running

To build and run these programs, Make sure you have [NASM][nasm] and [QEMU][qemu] installed.  
Then, you need to clone this repo, and run this command to build:  
`nasm -f bin -o boot.bin boot.asm`  
Then, to run the bootloader in qemu, run:  
`qemu-system-x86_64 boot.bin`  
If you're using VSCode, I have a build task set up for you, just press Ctrl+Shift+B and it will build and run the bootloader.  
And off to the races you go! (other than changing boot to your desired file name, of course)

## Resources to bounce off of when I get stuck

If this wasn't obvious already, these resources are not mine, and I do not take credit for them, nor can I guarantee that they are correct or safe.  
To learn ASM, I found [a tutorial playlist on YouTube][yt], and [The first link on google][firstlink].  
I have been using [OSDev][osdev] and [This Russian site I found on Google][russiansite] and a lot of [Wikipedia][wikipedia].  
Another resource is [This book][goodbook] and [This git repo that has short step-by-step instructions][nicegit].  
Found another nice interrupt list [here][anotherinterrupt], I've actually been using this one a lot.  
A [cool blog][coolblog] I found, and a [friendly discord server][notmydiscord].

## Another note

I'm using windows, which was my first mistake here, as QEMU doesn't play well, or at least the [binaries that were given on the website][winqemubin]. I tried compiling, and after a while, figured out that the DLLs were a bit funky. After a while of tinkering and getting close to caving in and downloading sketchy DLL files off the internet, I figured out that the version I downloaded was missing a DLL, [and rightly stated so in the changelog][changeloghighlight]. I downloaded the latest version, and it worked! I'm just going to leave this here in case anyone else has this problem.  
Please, **please** use Linux if you're up to this task, it will make your life so much easier, from running the binaries, to compiling with other tools. I'm avoiding it for the time being until i'm happily proficient with [Arch][btw].

## One more note

You should never, ***ever*** copy and paste code from anywhere, these resources are just to help you write your implementation. You should be writing your own code, even if it's uncanny how similar it is to these guides. You'll learn a lot from these guides, but you'll learn even more from experimenting and playing around with it!  
Also safety blah blah blah never copy code unsafe blah blah blah

## License

This repo, just like most of my other repos, is licensed under the [MIT License](LICENSE).

[yt]: https://www.youtube.com/playlist?list=PLetF-YjXm-sCH6FrTz4AQhfH6INDQvQSn
[firstlink]: https://www.tutorialspoint.com/assembly_programming/
[osdev]: https://wiki.osdev.org/
[russiansite]: http://vitaly_filatov.tripod.com/ng/asm/
[wikipedia]: https://en.wikipedia.org/wiki/BIOS_interrupt_call
[goodbook]: https://www.cs.bham.ac.uk//~exr/lectures/opsys/10_11/lectures/os-dev.pdf
[nicegit]: https://github.com/cfenollosa/os-tutorial/
[anotherinterrupt]: https://stanislavs.org/helppc/idx_interrupt.html
[nasm]: https://www.nasm.us/
[qemu]: https://www.qemu.org/
[coolblog]: https://pagekey.io/projects/pkos
[notmydiscord]: https://discord.com/invite/wVwG9J2Act
[winqemubin]: https://qemu.weilnetz.de/
[changeloghighlight]: https://qemu.weilnetz.de/#:~:text=2023%2D05%2D31%3A%20New%20QEMU%20installer%20(8.0.2).%20Added%20missing%20libssp%2D0.dll.
[btw]: https://www.google.com/search?q=i+use+arch+btw&tbm=isch
