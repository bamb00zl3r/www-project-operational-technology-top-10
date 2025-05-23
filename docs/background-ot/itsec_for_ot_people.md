# Security for OT: Why Is It Problematic?

While the term “operational technology” (OT) is fairly new, originating in the early 2000s, the underlying technology is not. Ranging back to mechanical control systems, industrial control systems (ICS) for example have come a long way. PLCs were already introduced in the 1960s, predating the first personal computer (the Apple 1 in 1976) by over a decade. Also, the integration with SCADA, starting in the 1980s, took place at the same time as the Internet was just beginning to become established more broadly.  This long-standing history created a very specific culture amongst the engineers and operators designing and using such systems, coming with its own tenets, views and best practices.

Naturally, at the onset of OT, malicious attackers were not a problem to be thought of – at that time they weren’t even for IT. But even when cyber-attacks finally materialized increasingly, they spared OT by large. The technology was difficult to understand and even more difficult to get access to, systems did not feature the kind of connectivity they do today and the attack surface to explore and exploit was far bigger and more rewarding on the IT side of things. It should come to no surprise therefore that in comparison to safety – which was and is paramount in OT – security was never a large concern historically. With operators coming mainly from an engineering background, they also did not pick up the cultural security changes that have manifested in the IT community over the last decades.

For quite a long time this did not prove to be problematic, attacks almost exclusively targeted IT systems. But then, in 2010, the discovery of Stuxnet sent shock waves through the security community, putting ICS and soon OT in general in an ever-increasing focus. Over half a century after the introduction of the first PLCs, the rate of occurrence of ICS-related attacks and malware started to rise steeply throughout the 2010s with the time between attacks ever decreasing since. Industroyer (2016), TRITON (2017), and Industroyer2 (2022) are just some of the most infamous attacks, showcasing how security incidents can degrade safety and availability – the traditional top concerns in OT.

While cultural security issues mentioned above still persist (but are decreasing), OT often suffers from additional structural and organizational problems when trying to tackle the growing threat from malicious actors. Many organizations simply cannot easily update or substitute vulnerable systems like it is mostly possible in IT. The adage “never change a running system” becomes even more true, if the system is a power plant for example, making major contributions to the national power grid and the regional power supply. It is simply not possible to shut down the whole plant on short notice to install an emergency patch for a newly detected vulnerability. Additionally, in comparison to IT, systems have a very long lifetime, exposing them to outdated software and subsequent known vulnerabilities even more.

All these factors and more – growing threat landscape, increasing connectivity in OT for more efficient management and operation, insufficient security – have lead governments and regulatory bodies around the world to introduce legislation effectively forcing the OT community to evolve their security culture and posture like IT has done over the last two decades.

## Common Problems and False Assumptions About OT Security

Changing cultures and even more so carefully engineered complex and critical systems like power plants, production sites and traffic control systems has the potential to cause friction and problems. This is totally understandable, as even in IT the introduction of new security technology and measures can create major pain points in the beginning. Nonetheless, neglecting security for a short-time saving of money and effort is a perfect setup for even more complications in the future when legislation tightens or if an actual attack happens, probably affecting availability and at worst even safety. Think about it that way: When security measures are planned and introduced, you dictate the circumstances, the execution time and potential downtimes.  But when you have to respond to a security-related incident the circumstances dictate everything. You then have very limited say in downtimes, required resources and above all the time when it has to happen.

To help with some common concerns and possible frictions, the following paragraph should address the most common complaints to alleviate the introduction of security in OT environments:

### Security vs. Safety

> We do not need security, we have more than enough safety mechanisms in place

As acknowledged before, safety is paramount – and with good reason! An exploding turbine affecting the lives of operators around it is undeniably more serious than a file server in an office getting encrypted by ransomware. Looking at safety in OT reveals how diligently the OT culture treats risk to life. Most of the time, there are multiple layers of safety mechanisms ensuring that even in face of failure of one layer, another one intervenes.

On a side note, this concept, commonly referred to as “defense in depth”, is also highly relevant to OT security. But even in face of these intricate safety mechanisms, think about cases where safety systems are explicitly targeted by malicious actors to prevent them from kicking in. Recall the aforementioned TRITON malware that explicitly targeted the safety systems of a petrochemical plant. In other words, security is an active enabler of safety. If security is compromised, this can pose a direct threat to safety systems and mechanisms. Therefore, safety and security cannot be seen as redundant but are two sides of the same coin trying to achieve the same goal – keeping the systems running in a safe state.

### Security vs. Availability

> We cannot harden/update systems to make them secure as we cannot afford the downtime

System availability is only second to safety in most cases, so naturally many systems cannot simply be taken down to introduce updates or change configurations. This is often hard to grasp for security professionals coming from an IT background. Every downtime has to be meticulously planned in advance. But this does not mean that downtimes are impossible in general. They do happen! Every component needs maintenance at some point in time and OT staff is usually highly experienced to align such maintenance downtimes with business goals and possibly existing regulatory requirements.

These time frames should therefore also be used to introduce security-relevant topics. To do so, a security roadmap detailing what measure can be implemented at what maintenance downtime has to be carefully crafted. As said before, this is your advantage when you tackle security in a pro-active way – you decide on when something happens! Of special concern is of course patch management, as on the one hand patches are usually released more often than there are maintenance downtimes and on the other hand older systems often do not receive them at all. With the former again careful planning goes a long way. By establishing a process rating the severity of a patch, updates and their urgency can be aligned with maintenance tasks.

So, unlike in IT, more uncritical patches can be postponed to a later point in time, while for critical emergency patches plans can be made in advance (often together with suppliers) on how to implement them. For the latter problem, the already mentioned “defense in depth” approach comes into play. Only because there are no direct patches for systems, it does not mean that there are no other security measures reducing the risk of a successful attack like, for example, careful network segmentation. By such “indirect measures” even systems that cannot be patched (yet) can be protected to an adequate level. This also helps in patch management in general, as patches can be postponed to a maintenance downtime easier when there are already other mitigations in place.

### Trusting the Blast Zones

> Our systems are isolated so there is no way to access them anyway. We therefore do not need further measures

Physical security and isolation are often a major strength in OT environments, far surpassing typical IT environments in that regard. Nonetheless, relying on access control alone can be deceptive. Surely, most environments won’t face the kind of intricacy and effort of nation-state attacks like Stuxnet (which breached air-gapped systems), but just think about a scenario, where an employee plugs in an USB stick that is privately owned. If the stick is infected with malware, your OT environment can be compromised soon – without any connection to the outside! This is a good case for “defense in depth” again: Physical access control and network segmentation are both important factors in a comprehensive security strategy. Without them, the strategy can barely be called comprehensive, but on their own they also are not sufficient for modern threat landscapes.

### Security vs. Performance

> We cannot afford to have any delays in network/system/etc. performance caused by security technology

This can indeed be a major problem. Especially OT protocols often cater to very specific performance requirements like real-time communication. As most of these protocols are quite old, security was not taken into account during creation. While there are some newer protocols with security features (like OPC UA) and some older ones offer security extensions (like PROFINET), these are often not supported by vendors or are not applicable to certain tasks. This should not discourage anybody from looking for alternative security measures.

If the protocol layer cannot be secured, then other mitigations like careful network segmentation or monitoring can significantly improve security posture. Especially as the OT security market is ever growing, more and more vendors are coming up with specific OT security products taking into account the complex requirements of many OT environments.  During the years-long experience of the authors of this document, there was never the case that there were no possible security improvements for the environment. Security is not a “one size fits all” product but has to be tailored to every system and environment, to find the best possible balance between security and performance/availability.

### Knowledge Gaps

> We are engineers, we do not have knowledge about security

This is also described in the beginning above. OT staff has in general a completely different background and view on security/safety than IT staff. While this at first seems to be a hindrance, it does not have to be that way. In-depth OT-specific knowledge is crucial in securing OT environments as well as in detecting and responding to security incidents. Typically, the engineers working with the systems are the first to notice strange behavior, being the primary source of (human) detection of attacks. They also know the specific characteristics, the requirements and the processes coming with their systems. Without this knowledge it is nigh impossible to craft a tailored security strategy like described above. The lack of security know-how can be tackled in several ways and depends on the organization of the company/organization: If there already is security personnel and no specific OT security team is planned, a closer collaboration between IT and OT staff can lead to greater understanding on both sides.

Experience has shown that IT security staff can come up with viable solutions for OT security problems once they have grasped the difference between IT and OT. For this you may refer them to the chapter “OT for IT Sec People”. OT staff on the other hand do not have to become in-depth security experts in this case. Enabling them to think like an attacker and see potential vulnerabilities beforehand can go a long way. OT personnel already work with (safety) risks every day, so the required mental effort to also deal with risks that are introduced on purpose is often not that high.

There is also a steady increase in educational material for OT security, be it in the form of free documents on the Internet or in the form of instructor-led training programs. Such training programs can also be of value in the case of bigger organizations that decide to establish specific OT security teams. This of course leads to subject matter experts that combine the best of both worlds, but it takes a lot of time and money to train such a team. Whatever fits your organization, it must be explicitly noted that giving additional security tasks to an already overworked staff is a recipe for disaster. Management must ensure that there are enough resources for those responsible. Security is not something that can be done besides!

### Security by Obscurity

> We are a small power plant/production site/or similar. Nobody will make the effort to attack us

This is a sentiment that is often also shared by IT. Plain and simple, this is a dangerous fallacy that does not resemble ongoing threats. While sophisticated nation-state attacks surely affect only a very small subset of all OT environments, threat reports show that the awareness of malicious actors – be it criminal, be it hacktivists – for OT is on the rise. While not nearly as dangerous as advanced threat groups, also rudimentary malware can lead to disruption and availability issues. One especially concerning trend is the rise of OT ransomware, a type of malware that has been haunting IT for years now. In general, more and more OT incidents do not happen because of a specific interest in the target, but due to opportunism and the chance to extort money or amplify a certain political message  by attacking a coincidentally vulnerable OT environments (e.g. think of a newly vulnerable remote access solutions that has to be reachable over the Internet).

### Problems with the supply chain

> Even if we want to integrate security more, many of our suppliers do not feature security in their products

Yes, this can be a problem. While regulations force more and more vendors to consider security in their new products, this does not help with already existing systems. Nonetheless, security can be done in many ways and as described before, there are security workarounds for almost all problems.  “Defense in depth” is again the keyword to look for. If there is no security control for one specific component (e.g. a PLC), then the additional layers of a DiD approach can provide security by for example monitoring the network of the PLCs, restricting access to this network segment, providing strict access control for engineering via dedicated and isolated workstations and so on.

## Advantages of Security  

All in all, when security is done the right way, it should never be a hindrance, but an enabler to a resilient, available and safe OT environment. While a meticulously tailored security strategy ensures compliance with existing and upcoming legislation and regulations, truly living the strategy brings many operational advantages, some of which are:

- Higher confidence in safety of systems as deliberate attacks against safety systems is made more difficult
- More resilient infrastructure leading to less downtime of systems in case of an incident
- Greater insight in existing assets as a result of needed analyses of status quo
- Easier manageability of networks due to appropriate segmentation
- More insight into network traffic due to increased monitoring – not only security-related incidents can be detected and handled faster
