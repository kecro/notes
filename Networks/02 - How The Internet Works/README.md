# [How The Internet Works ?](https://www.youtube.com/playlist?list=PLzdnOPI1iJNfMRZm5DDxco3UdsFegvuB7)

## Table of Contents

- [Wires, Cables & Wifi](https://github.com/kecro/notes/tree/master/Networks/02%20-%20How%20The%20Internet%20Works#wires-cables--wifi)
- [IP Addresses & DNS](https://github.com/kecro/notes/tree/master/Networks/02%20-%20How%20The%20Internet%20Works#ip-addresses--dns)
- [Packets, Routing & Reliability](https://github.com/kecro/notes/tree/master/Networks/02%20-%20How%20The%20Internet%20Works#packets-routing--reliability)
- [HTTP & HTML](https://github.com/kecro/notes/tree/master/Networks/02%20-%20How%20The%20Internet%20Works#http--html)
- [Encryption & Public Keys](https://github.com/kecro/notes/tree/master/Networks/02%20-%20How%20The%20Internet%20Works#encryption--public-keys)
- [Cybersecurity & Crime](https://github.com/kecro/notes/tree/master/Networks/02%20-%20How%20The%20Internet%20Works#cybersecurity--crime)
- [How Search Works](https://github.com/kecro/notes/tree/master/Networks/02%20-%20How%20The%20Internet%20Works#how-search-works)

In the early 70s, **Vint Cerf** and **Bob Kahn** work on the design of what we called the Internet.

It was a result of another experiment called the **ARPANET** *which stood for **A**dvanced **R**esearch **P**roject **A**gency **N**etwork*.

The **Internet** is made up of an incredibly large number of independently operated networks.

The utility of the net is that any device can communicate with any other device and move information.

> What's interesting about the system is that it's fully distributed. There's no central control that is deciding how packets are routed or where pieces of the network are built or even who interconnects with whom. These are all business decisions that are made independently by the operators.

In conclusion, **the Internet is a network of networks** and thereby **anybody** and **everybody** are in charge of it.
***

## [Wires, Cables & Wifi](https://www.youtube.com/watch?v=ZhEf7e4kopM&list=PLzdnOPI1iJNfMRZm5DDxco3UdsFegvuB7&index=2)

### How does a picture, text message or email gets sent from one place to another ?

The **Internet** is a lot like the **postal service** !

However, instead of boxes and envelopes the Internet **ships binary information**.

**Information is made of bits** *like we saw in* [How Computers works ?](https://github.com/kecro/notes/tree/master/Networks/01%20-%20How%20Computers%20Works#binary--data).

```
8 bits = 1 byte
1024 bytes = 1 Ko (kilobyte)
1024 kilobytes = 1 Mo (megabyte)
```

Today we **physically send bits** by **electricty, light and radio waves**.

___

#### *... how can we send five zeros in a row ?*

The solution is to introduce a clock or a timer.

The operators can agree that the sender will send one bit per second, the receiver will sit down and record every single second and see what's on the line.

Obviously we'd like to send things a little bit faster than one bit per second so we need to increase our **bandwidth**.

**Bandwidth** : maximum transmission capacity of a device.

**Bandwidth** is measured by **bit rate**.

**Bit rate** : number of bits that we can send over a given period time *usually measured in seconds*.

**Latency** (*different measure of speed is the latency*) : times it takes for a bit to travel from one place to another.

___

#### *... what sort of cable to send these messages over ? and how the signals can go ?*

With an **Ethernet wire**, you see really measurable signal loss over just a few hundred feet.

If we want the Internet to work over the entire world, we need a different way of sending this information really long distances (*across the oceans for instance*).

**Light** move faster than **Electricity**.

A **Fiber optic cable** is a thread of glass engineered to reflect light.

With a **Fiber optic cable**, we can send bits as light beams from one place o another.

___

#### *... how do we send things wirelessly ?*

**Wireless bits sending machines** typically use a radio signal to send bits from one place to another.

The machine **translate** the **ones and zeros** into **radio waves** of different frequencies.

The receiving machines reverse the process and convert it back into binary code.
___

## [IP Addresses & DNS](https://www.youtube.com/watch?v=5o8CwafCxnU&index=3&list=PLzdnOPI1iJNfMRZm5DDxco3UdsFegvuB7)

### IP Addresses

The Internet is a design philosophy and a architecture expressed in a set of **protocols**.

**Protocol** : set of rules and standards used to communicate between machines.

All the different devices on ther Internet have **unique addresses** which are just numbers like phone numbers.

One of the most important protocols used in Internet communication simply call **IP** (**I**nternet **P**rotocol).

Just like a home address has a country, a city, a street, and a house number, an **IP adress** has many parts.

- **Earlier numbers** usually **identify** the **country** and **regional** network of the device.
- Then come the **subnetworks**.
- And finally the adress of the **specific device**.

This is the **IPv4** version, designed in **1973** and adopted in the **1980**'s and provides more than 4 billion unique adresses.

**IPv6** has recently appeared to fill the void of available addresses. It uses **128 bits**/**16 bytes** per address and provides over **340 undecillion unique addresses**.

> 3,4 x 10^38 équivaut à un nombre illimité puisque pour saturer le système, il faudrait placer plus de 667 millions de milliards d'appareils connectés à internet sur chaque millimètre carré de surface terrestre.

___
### DNS
A system called **DNS** or **D**omain **N**ame **S**ystem associates names like [www.example.com](http://www.example.com) with the corresponding addresses.

You must know that there is no way one DNS Server can handle all the requests from all devices.

DNS Servers are connected in a distributed hierarchy and are divided into zones, splitting up reponsabilities for the major domaines such as **.org**, **.com**, **.net** etc.

**DNS Spoofing**, also referred to as **DNS cache poisoning**, is an attack when a "*hacker*" taps into a DNS Server and changes it to match a domain name with the wrong IP address.

---
## [Packets, Routing & Reliability](https://www.youtube.com/watch?v=AYdF7b3nMto&index=4&list=PLzdnOPI1iJNfMRZm5DDxco3UdsFegvuB7)

If the Internet were made of direct, dedicated connections, it would be impossible to keep things working as millions of users join.

>Especially since there is no guarantee that every wire and computer is working all the time.

---
### Packets

Data travels on the Internet in a much less direct fashion. Informations goes from one computer to another, in what we called a **packet** of information.

And a **packet** travels a lot like you get from one place to another in a car, depending on :
- traffic congestion
- road conditions

You might *choose* **or be forced** to take a different route to get to the same place each time you travel.

And just as you can transport all of stuffs inside a car, many kinds of digital information can be sent with **IP Packets** (*Music, E-Book, Videos...*), but __there are some limits__.

> **Example :** *What if you have to send a space shuttle from where it was built to where it will be launched ?*
The shuttle will not fit in one truck, so it needs to be `shrunk` (*broken down*) into pieces, transported using a fleet or trucks. They could all take different routes and might get to the destination at different times. But once all pieces are there, you can reassemble the pieces into the complete shuttle.

Each packet has the **IP** (*internet address*) of __where it came from and where it's going !__

---
### Routers

Special computers called **Routers** act like traffic managers to keep packets moving through the networks smoothly.

As part of the **Internet Protocol**, each routers keeps track of **multiple paths** for sending packets, and it chooses the **cheapest available path** for each piece of data, *based on destination IP address of the packet*.

**Cheapest** in this case doesn't mean ~~cost~~, but __time and non-technincal factors such as politics and relationships between companies.__

>Often the best route for data to travel isn't necessarily the most direct !

Having __options__ for paths makes the network __fault tolerant__. Which means the networks can keep sending packets even if something goes horribly wrong.

![Broken routes](Something_Horrible.png)

---
### Reliability (a key principle of the Internet)

**TCP** or **T**ransmission **C**ontrol **P**rotocol, manages the sending and recieving of all you data as packets.
> Unlike **UDP** which is connectionless.

![TCP](TCP.png)

Which is great about the **TCP and Routers** system is they're **scalable**. They can work with 8 devices or 8 billion devices.

In fact, because of these principles of fault tolerance and redundancy, the **more routers** we add, the **more  reliable** the Internet becomes.

---
## [HTTP & HTML](https://www.youtube.com/watch?v=kBXQZMmiA4s&list=PLzdnOPI1iJNfMRZm5DDxco3UdsFegvuB7&index=5)

>The Internet is completly open. All of its connection are shared and information is sent in plain text.
This makes it possible for "hackers" to snoop on any personal information that you send over the internet.

Safe websites prevent **snooping** and **tampering**, by asking your web browser to communicate on a secure channel.

When you see this little lock in your Web Browser address bar :

![secure green lock](secure_lock.png)

It mean that the website is using **HTTPS** (**H**yper **T**ext **T**ransfer **P**rotocol) and more precisely :
- **SSL**(***S** ecure **S**ockets **L**ayer*)
- and its successor **TLS** (**T**ransport **L**ayer **S**ecurity).

___
### Certificate

When a website asks your browser to engage in a secure connection, it first provides **a digital certificate**.
**A digital certificate** is an official ID card proving that it's the website it claims to be.

> Digital certificates are published by certificate authorities, which are trusted entities that verify the identities of websites and issue certificates for them. Just like a government can issue IDs or passports. Now if a website tries to start a secure connection without a properly issued digital certificate, your browser will warn you.

___
## [Encryption & Public Keys](https://www.youtube.com/watch?v=ZghMPWGXexs&list=PLzdnOPI1iJNfMRZm5DDxco3UdsFegvuB7&index=6)

An average computer today, would take just a few seconds to try all 10 billion possibilities.

### How can you encrypt messages so securely that they're too hard to crack ?

Now **"too hard"** means that there are **too many possibilities to compute in a reasonable amount of time**.

Today's secure communications are encrypted using 256 bit keys. That means a bad guy's computer that intercepts your message would need to try this many possible options... until they discover the key and crack the message.

Even if you had a 100,000 super computers and each of them was able to try a million billion keys every second it would take trillions of trillions of trillions of years to try every option, just to crack a single message protected with 256 bit encryption.

> Of course computer chips get twice as fast and half the size every year or so. If that pace of exponential progress continues, today's impossible problems will be solvable just a few hundred years in the future and 256 bits won't be enough to be safe.

The good news is, **using a longer key doesn't make encrypting messages much harder**, but **it exponentially increases the number of guesses that it would take to crack a cipher**.
___
### Asymetric Encryption

Nowadays, computers use **Asymmetric keys**, a **public key** that can be exchanged with anybody and a **private key** that is not shared :
- The **Public Key** is used to **encrypt data** and anybody can use it to create a secret message.
- The **secret** can only be **decrypted** by a computer with access to the **private key**.
___
## [Cybersecurity & Crime](https://www.youtube.com/watch?v=AuYNXgO_f3Y&list=PLzdnOPI1iJNfMRZm5DDxco3UdsFegvuB7&index=7)

**Jenny Martin**, the director of cybersecurity investigations at Symantec said "*the next World War may not be fought with traditional weapons, but with computers used to shut down national water supplies, energy grids, and transportation systems.*"

___
## [How Search Works](https://www.youtube.com/watch?v=LVV_93mBfSU&index=8&list=PLzdnOPI1iJNfMRZm5DDxco3UdsFegvuB7)

Let's ask a simple question."How long does it take to travel to Mars?"

### ...*where did these results come from and why was this listed before the other one?*

When you do a search, the search engine isn't actually going out to the World Wide Web to run your search in real time !

So to make your search faster, search engines are constantly scanning the web in advance to record the information that might help with your search later.

### "Spiders"

The internet is a web of **pages connected to each other by hyperlinks**.

Search engines are **constantly running** a program called **"spider"** that **crawls through** these web **pages** to **collect information** about them.

Each time it finds a hyperlink, it follows it until it has visited every page it can find on the entire internet.

For each page of the spider visits, it **records** any information it might need for a search by adding it to a **special database** called a **search index**.

### Ranking Algorithms

When you ask "how long does it take to travel to Mars", the search engine looks each of those words in the search index to immediately get a list of all the pages on the internet containing those words.

But just looking for these search terms could return millions of results...

The search engine's **ranking algorithm** might check :
- if your search term shows up in the page title
- if all of the words show up next to each other

or any number of other calculations that helped it better determine which pages you'll want to see and which you won't.

Google invented the most famous algorithm for choosing the most relevant results for a search, by taking into account how many other web pages link to a given page.

The idea is that if lots of websites think that a web page is interesting, then it's probably the one you're looking for.

> This algorithm was called "Page Rank", not because it ranks web pages, but because it was named after its inventor, Larry Page, who is one of the founders of Google.

# Conclusion

<div style="text-align:center">
    <img src="Conclusion.png" alt="Conclusion image" />
</div>
