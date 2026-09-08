+++
title = "homelab on a budget"
date = 2026-08-30

[taxonomies]
tags = ["technical"]
+++

turns out a lot of my coworkers homelab. found this out through a random conversation at work. a couple of hilariously intense examples: our boss (yes, the associate director) has an entire server rack he's trying to sell because he's upgrading, and another coworker has a server, gnss, and lidar on his crosstrek (note: it's a hobby project he's doing for fun. not work related). we got to talking about who else does this kind of thing, and it was way more people than i expected. i just didn't have a way in yet.

then the coworker who put lidar and gnss on his crosstrek handed me a cisco asa 5512-x like it was nothing. i grabbed a compatible 2.5" sata ssd for it and figured that'd be the extent of it.

![cisco asa 5512-x](/img/homelab/cisco-asa-5512x.jpg)

from there something clicked, probably one of those 2am late night highs, and i went all in.

turns out you don't need much to start. a raspberry pi is plenty. i dug through my old box of microcontrollers, sensors, and other embedded systems junk and found my old pi 3b, a 16gb microsd card, and some leftover fiber optic cable just sitting there. jack pot!

![oh yeah](/img/homelab/koolaid.jpg)

that pi became the first real piece of the homelab, running pihole (i'm fed up with ads) and wireguard so i could vpn in from anywhere once everything else came online. pihole won't touch youtube ads though, brave handles those instead.

for compute, i pulled my old toshiba laptop out of the closet and turned it into my proxmox box / lab manager. not sure it's the wisest long-term call, but it's what i had lying around. well... now that i have all this i should probably figure out how to put the cisco asa 5512-x to use instead of letting it sit there without a rack. i'll probably improvise a rack by buying stuff from ikea. once that's sorted i'll basically have a full stack, minus a nas and a proper workstation. those are getting bought gradually, because i'm a new grad and my bank account would like a word... or who knows maybe i'll buy the server that my boss is selling.

