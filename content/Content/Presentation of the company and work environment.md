---
title: Presentation of the company and work environment
draft: false
tags:
---
# IBA (Ion Beam Applications)**

## **Introduction to IBA**

- **Company Overview**: IBA, or Ion Beam Applications, is a Belgian company founded in 1986. It is a global leader in advanced cancer therapy technologies, specializing in particle accelerators and proton therapy solutions. IBA’s mission centers on improving cancer treatment, diagnostic techniques, and other medical and industrial applications by leveraging innovative particle-beam technologies.
- **Global Presence**: IBA operates in over 40 countries worldwide, with headquarters in Louvain-la-Neuve, Belgium, and a presence through subsidiaries and partnerships across Europe, North America, Asia, and more. This international reach allows IBA to provide comprehensive support and solutions to healthcare facilities worldwide.
- **Market Leadership**: IBA is recognized as a leader in the field of proton therapy, a precise and effective treatment modality for various types of cancer. Its market share in proton therapy equipment and related technologies makes it a pioneering force in oncology.

## **Core Business Areas**

- **Proton Therapy**: IBA is primarily known for its proton therapy solutions, providing cutting-edge systems and software that enable accurate targeting of cancerous tissues while minimizing damage to surrounding healthy tissue. This technology is especially valuable for treating pediatric cancers and complex tumors.
- **Particle Accelerators**: Besides medical applications, IBA also develops cyclotrons and other particle accelerators for diagnostic imaging and industrial use. Its machines are essential for the production of radioisotopes used in PET and SPECT scans, crucial for cancer and cardiovascular disease diagnostics.
- **Dosimetry Solutions**: IBA produces dosimetry equipment to measure and control radiation doses, ensuring safety and accuracy for both patients and medical personnel. This division serves both proton therapy and conventional radiation therapy markets.
- **Industrial Applications**: Beyond healthcare, IBA’s accelerators are used for sterilization, material modification, and imaging technologies applied in industries like food safety and materials research.

## **Mission and Values**

- **Mission**: IBA’s mission is to protect, enhance, and save lives by innovating in particle therapy and radiation treatment. The company is committed to advancing medical technologies and ensuring patient safety.
- **Core Values**: Innovation, safety, quality, and sustainability are central to IBA's values. The company prioritizes continuous research and development, rigorous safety standards, and environmental responsibility.



# Work environnement

## **Company Organigram**

As explain above, IBA have multiple core business and the main one is the proton therapy. It is in this division that i have worked. 
I worked in the software engineering department of the R&D group.

![[WhatsApp Image 2024-10-31 à 10.07.55_0eda3eb9.jpg]]




# Software engineering department 


The development of the main product software, proton therapy, takes place primarily in the Software Engineering Department. This department is divided into four teams **Beam**, **Imaging**, **Workflow** et **Positioning** and consists of around 60 people. I was integrated in the **Beam** Team. Gregory was my responsable and even though it's not visible on the following graphs, Gregory is Adrien's manager who were also in the Beam team. 
![[orgchart3.pdf|500x500]]

## Beam
The Beam software R&D team is responsible for the development of the software for the beam line. The beam line is the part of the proton therapy system that lies between the particle accelerator and the patient, ensuring that the particle beam is properly directed into the treatment room.

As explained [[Description of the work flow#Main Product workflow|here]], the team receive instruction and requirements from the PESS team.
The team manager oversees task allocation, ensuring that each task has enough resources. He regularly checks in with team members to assess if they are facing any major issues. The architect, on the other hand, is responsible for the overall structure of the code and integrates the various parts created by different team members, ensuring that they work together seamlessly within the larger system.

## Gregory Deschamps
Grégory has a basic knowledge of computing, which allows him to follow the team's discussions, but he isn’t a developer by training. His primary role is team and people management, making sure that no one is stuck on particular tasks and helping circulate information among team members, who might sometimes be deeply absorbed in their own work.

He also plays the role of a "coach." He conducts regular one-on-one meetings with team members, during which they can discuss their experiences, concerns, and any issues they’re facing. Together, they set personal development goals to help team members improve in areas where they feel they need growth.

Grégory is exceptionally welcoming and attentive. From my initial interview through the end of my internship, I always found him to be supportive and pleasant. His openness and kindness helped me feel comfortable and integrated within the team right from the start, for which I am genuinely grateful.
## Adrien Faucon
Adrien was my supervisor throughout the entire internship, and he played a crucial role in my development during this time. He was the person I spent the majority of my time with, working closely together on the [[Expected deliverables|ProteusToolbox]] project.

He is a **Non-product software owner** and is responsible for software that supports internal operations but is not part of the primary medical products offered to clients. This software includes internal tools, support applications, and utilities used for development, testing, or managing main products, like proton therapy systems, but is not directly involved in patient treatments.

The NPS owner’s responsibilities generally include:

1. **Quality control and supervision**: Ensuring non-product software meets internal quality standards.
    
2. **Management of release and access**: Approving updates or new versions to make sure only reliable, functional software is available to internal teams.
    
3. **Risk assessment**: Evaluating any potential risks associated with the use of NPS, especially if it interacts with medical systems, to ensure it doesn’t impact patient safety.
    

In essence, the NPS owner acts as a **manager and quality gatekeeper** for non-product software, maintaining reliability and documentation without the rigorous validation required for medical products.

The [[Expected deliverables|ProteusToolbox]] is by essence a non-product Software which falls in to the responsibility of Adrien. This is the reason i was integrated in his team.

Adrien was instrumental in the success of my project, always available to answer my questions and think through possible solutions with me. While he didn’t code directly, he acted as my co-pilot, offering a valuable perspective on the project. He frequently took a step back to assess our progress and proposed alternative solutions, as well as potential new features to implement.




## Valentin Demonte (intern Client)

Valentin Demonte is a flying engineer that created the first version of the [[Expected deliverables#ProteusToolBox|ProteusToolbox]]. 
**Flying Engineer** at **IBA** (Ion Beam Applications) travels to various medical facilities to install, maintain, and support IBA equipment, such as those used in proton therapy for cancer. They are responsible for training medical staff on system operation and ensuring optimal performance through preventive maintenance and troubleshooting. They require strong electrical engineer background. 

As explained in the mentioned section above, Valentin and his team developed python scripts to automate some testing and maintenance process. He then created the ProteusToolbox to help he and his team to easily dispose of all those scripts. 

Valentin is an electrical engineer by training and didn't have much formal development experience from university, but he learned on the job because he enjoys it. The first version of the ProteusToolBox was, in my opinion, more than qualitative, and I was able to reuse a significant portion of it.

Since this application is essentially "his," and its primary target audience is his team, he was actively involved throughout the entire development process. He attended our weekly meetings even while traveling, providing feedback on our proposals and detailing the actual user needs, which is essential for the project's success. This close collaboration was crucial, although the broader vision from Adrien to scale the application led to some minor tensions between him and Valentin toward the end.