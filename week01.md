# Week 1

[Return to contents](README.md)

---

## Lecture Notes - Cryptographic Concepts, Terminology & Tools
--
I wrote out all the lecture concepts by hand because I find writing stuff out helps me remember it way better than just reading slides. My notes cover the CIA Triad, AAA Model, the encryption model with the formulas, symmetric vs asymmetric, and Caeser cipher worked examples.

![Encryption Model and Learning Outcomes](images/w01-notes-encryption-model.png)
![CIA Triad, AAA, Symmetric vs Asymmetric](images/w01-notes-cia-aaa-symmetric.png)
![Caesar Cipher Worked Examples](images/w01-notes-caesar-cipher.png)

I also used mermaid.js to help me make cleaner flowcharts and tables for my notes since drawing them by hand wasn't hte best for more complex diagrams.

---

## Tutorial Tasks
### Setting up VirtualBox and PuTTY

This part was pretty easy for me. I already had VirtualBox and PuTTY set up from my System and network Admin unit (COIT12146) that I'm also doing this term, so it was just the same thing again. The only thing I had to do was to create another VM on VirtualBox. I've added a new Port forwarding rule with SSH (`127.0.0.1:2201` pointing to guest port `22`).

I've also used LInux before - I rented a server from Oracle Cloud a while back and had to use the command line to set up a VPN on it. I was googling every command back then but it got me comfortable enough with the basics like `cd`, `ls`, `nano` etc.

![PuTTY connected to my VM](images/w01-putty-connected.png)

### SSH Key Generation
This was honestly the hardest part of the week for me. I couldn't get into the 2026 tutorial recording on Moodle so I was watching the 2024 Echo360 recording by Steve Gordan, and the steps didn't exactly match up with what I needed to do.

I kept trying different things in PuTTY until I figured out the right command:

```bash
ssh-keygen -t ed25519 -C "anshul.bairy@cqumail.com"
```

Then I had to get the public key and put it on GitHub:

```bash
cat ~/.ssh/id_ed25519.pub
```

Copied the output (in PuTTY you just select the text and it copies automatically, which I didn't know at first) and pasted it into GitHub under SEttings > SSH Keys.

![SSH key generation](images/w01-ssh-keygen.png)

Tested it with:
```bash
ssh -T git@github.com
```

And it worked, got the "successfully authenticated" message.

![SSH test success](images/w01-ssh-test-success.png)

The thing that clicked for me here was that this is literally the asymmetric encryption stuff from the lecture but in practice. Private key stays on my machine, public key goes to GitHub. They verify each other mathematically instead of using a password. Before doing this I understood the concept from the slides but it didn't really make sense until I actually did it.

### Git Clone, Commit, Push
This was easy since I've been using Git for about a month now for my personal notes. Cloned both my journal repo and the unit's private repo:
```bash
mkdir git
git clone git@github.com:
