In 2017, I won DerbyCon’s Social Engineering Capture the Flag (SECTF). This exercise pit me and five other competitors against an unknowing Fortune 500 business in the Louisville, KY area. We spent three weeks collecting OSINT, followed by 20 minutes in a (mostly) soundproof booth to vish the target company’s employees. While researching my target company, I checked an executive’s social media accounts and learned that he’d been late to a business meeting in Amsterdam because an airline had delayed his flight in Newark. This seemingly harmless piece of information gave me the perfect excuse for contacting him.

With this knowledge, I added that airline’s phone number to my list of numbers to vish. I then acquired the executive’s name, email address, and phone number, and added those to my list of targets. Had this been an engagement allowing phishing, I would have sent an apology email that mimicked the airline’s template, and then followed up with a phone call, pretending to be the airline. Then I could have confirmed the information I already knew and asked “security questions” to convince the target that I was a trusted source. I might have even incorporated a few Windows operating system sounds to amplify my credibility. Finally, I would have asked him potentially lethal questions about the company’s operating environment, such as the status of equipment upgrades, operating schedules, or other company-specific confidential data.

#### Employees of the Company

A separate page lists LinkedIn users who are employees of the company. Use this to see the role each person plays. For example, Figure 5-3 shows someone with the job title _intrusion analyst_, a cybersecurity role that suggests the company actively monitors its websites and networks for malicious behavior.

We can assess the security of the company via its number of information security employees. An easy way to accomplish this is to look through employee profiles for certification acronyms. Checking for CISSP, GPEN, OSCP, CEH, and Security+ are good starting points. Good job titles to search for include the terms _information security, cybersecurity, intrusion,_ and _CISO_.

These employee profiles also tell us about the technologies that the company uses. By searching them, we can detect the presence of security event and incident management (SEIM) solutions, malware protections, email filtering, or VPNs. Additionally, they help us build an email list for further profiling and phishing.

#### Customers and Public Sentiment

When vishing a company, one of the slyest ways to get an employee to actually talk to you is to pose as a customer. You can find a myriad of real customers by looking at Facebook’s Community tab and reading reviews. In Figure 5-7, Walmart’s Community tab shows various posts to the page by the general public. These should be taken with a grain of salt and in context. Some of these posts are legitimate concerns, but others are conspiracy theories, unfounded claims, attempts at going viral, and reports of fake or impersonating pages.

#### Finding Geotagged Posts

Next, leave the company’s Instagram page and search Instagram for the company’s office address. This leads us to all posts _geotagged_ at this address. Geotagging occurs automatically when both a device and an app’s location services are enabled. The location will be embedded into the post and become a searchable field. From the returned pictures, you’ll likely find two very useful bits of information: company badges and pictures from the employees’ desks.

One particularly useful form to look at is SEC Form 10-K, which is the company’s annual report. It provides an overview of how the company is doing financially, the executive team, the board of directors, any problems they had over the past year, and risks that concern them. The SEC mandates that companies file these forms within 90 days of the end of their fiscal year, so publication dates may vary.

**A statement about changing the business name from _Walmart Stores, Inc._ to _Walmart Inc._**

1.  This could be useful in engaging with employees and vendors alike.

**A section called “Risks Factors and Uncertainties Affecting Our Business”**

1.  This is an excellent reference that will help an attacker understand the company’s business model and how it perceives threats.

**A list of websites that Walmart uses to conduct business on the internet**

1.  Here, we also see what Walmart considers to be its competition. In the section about its warehouse membership Sam’s Club, for instance, it mentions Costco.

**A list of key people**

1.  This list of high-level employees could be used in vishing and whaling attacks. We also see the employees’ roles and ages, which might help monitor their social media.

**A discussion of how Walmart uses technology**

1.  This enables us to see how it mitigates and perceives threats associated with its information technology infrastructure.

**Insight about Walmart’s legal activity**

1.  This can give us additional context for the way the company operates or help us target someone in the legal department.

**Information about the auditing firm that performed an independent, third-party audit**

1.  This gives us further context for our pretext.

**Introductions of the board of directors and their backgrounds**

1.  This provides us with more information about how Walmart does business. It also provides us with information we could use to build believable pretexts to use against their associates.

Other forms you should look for are 8-K (change in material status) and 10-Q (quarterly report). The 8-K typically involves the awarding or selling of shares of stock. The 10-Q is an incremental version of the 10-K produced quarterly, but in lesser detail.