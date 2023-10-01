(this is a backup of https://github.com/opensystm/handshake-micro-grants/issues/5)

# The most powerful Handshake seed node

Problem
---

Each Handshake client depends on seed nodes and other listening full nodes to work. At the moment of writing based on https://shakenodes there are only two reachable Handshake nodes in APAC which is home to 60 per cent of the world's population. There are many reachable Handshake nodes in United States, United Kingdom and Germany though.  

<img width="879" alt="Screenshot 2023-10-01 [shakenodes](https://shakenodes)" src="https://github.com/opensystm/handshake-micro-grants/assets/104037912/6ab5ff07-b7cd-4ff9-bc75-cdb5bc2d975e">

What will you be building? Why is that a valuable open source contribution to Handshake?
---

I'm going to setup a powerful reliable seed node that allows inbound connections from a variety of Handshake clients in Mumbai for at least three years. Such a seed node is the backbone of a healthy network. Read an answer from ChatGPT in the next comment below.


What have you built previously?
---

https://github.com/handshake-enthusiast/handshake-enthusiast#readme


What are completion criteria?
---

A listening Handshake full node  
- that accepts inbound connections from other [`hsd`](https://github.com/handshake-org/hsd) full nodes like [Bob wallet](https://bobwallet.io/) and light clients running [`hnsd`](https://github.com/handshake-org/hnsd) like [Fintertip](https://impervious.com/fingertip) or `hsd --spv` like Bob wallet in SPV mode  
- using the latest hsd version ([6.1.0](https://github.com/handshake-org/hsd/releases/tag/v6.1.0) at the moment of writing)
- with _/6.1.0/handshake-micro-grants/_ as a public [user agent](https://github.com/handshake-org/handshake-org.github.io/pull/164/files) 
- with uptime monitoring
- hardcoded into the [hsd](https://github.com/handshake-org/hsd/blob/master/lib/net/seeds/main.js) and [hnsd](https://github.com/handshake-org/hnsd/blob/master/src/seeds.h) seed nodes
- constantly present on https://shakenodes and in https://hnsnodes.htools.work/api/v1/snapshots/latest/reachable
- with 16 GiB and 4 vCPU using the latest generation general purpose [Amazon EC2 M7g instance](https://aws.amazon.com/ec2/instance-types/m7g/)

When will this be completed (max 4 weeks)?
---

Within a few days after the grant is awarded.

What is your contact information?
---

_Email:_ turbine_verbose0s@icloud.com

Notes
---

- I've sent you a gist link to a detailed article draft on how to host such a listening full node. I plan to publish a series of posts in the near future to help others set up full nodes that allow inbound connections.  
- Similar work [was done](https://www.reddit.com/r/handshake/comments/poo5iw/each_handshake_node_depends_on_other_listening/) by another community member a couple years ago. I learnt a lot from it.

---

[_ChatGPT_] Here's a detailed answer to the question "Why is that a valuable open source contribution to Handshake?":

---

Setting up a powerful and reliable seed node in Mumbai, especially in a region like APAC which is home to 60% of the world's population, offers several significant benefits to the Handshake network:  
1. **Network Resilience and Decentralization:** One of the core principles of blockchain and decentralized networks is to avoid central points of failure. By increasing the number of seed nodes, especially in underrepresented regions like APAC, we enhance the network's resilience against potential attacks, outages, or disruptions.
2. **Improved Network Performance:** With a seed node in Mumbai, local Handshake users in the APAC region can connect to a closer node, reducing latency and improving transaction speeds. This ensures a smoother and more efficient user experience for a significant portion of the global population.
3. **Increased Adoption:** A robust and efficient network can encourage more users and developers in the APAC region to adopt and build on Handshake. This can lead to increased network activity, more decentralized applications, and a broader user base, further strengthening the Handshake ecosystem.
4. **Open Source Collaboration:** By contributing this as an open-source initiative, we're not only strengthening the network but also setting a precedent for community-driven enhancements. It encourages other community members to contribute, share knowledge, and collaborate on further improvements.
5. **Educational Value:** Alongside the seed node setup, the associated documentation and articles can serve as valuable resources for others in the community. This educational aspect can demystify the process of setting up nodes, encouraging more community members to participate actively in network maintenance and growth.
6. **Geographical Diversification:** Blockchain networks thrive when they are geographically diverse. By setting up a node in Mumbai, we're ensuring that the Handshake network is not overly reliant on nodes from specific regions, like the US, UK, or Germany. This geographical diversification is crucial for a truly global and decentralized network.
7. **Future Growth:** APAC, with its vast population and rapidly growing tech sector, represents a significant opportunity for Handshake's expansion. By establishing a strong presence now, we're laying the groundwork for future growth and adoption in the region.  

In conclusion, this contribution is not just about adding another node; it's about enhancing the Handshake network's resilience, performance, and potential for growth. It embodies the spirit of open-source collaboration, where community members proactively identify gaps and work towards filling them for the benefit of all.


