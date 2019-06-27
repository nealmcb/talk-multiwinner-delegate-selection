class: center, middle

### Risk-Limiting Audits: Lessons Learned

Neal McBurnett [@NealMcB](https://twitter.com/nealmcb)

At the 2018-12-07 [MIT Election Audit Summit](https://electionlab.mit.edu/election-audit-summit)
---
class: left

## Neal McBurnett
* Consultant
* ColoradoRLA project team member with Democracy Works and Free & Fair
* Speaking for myself
* Working on election audits and integrity since 2003
 * Poll worker
 * Volunteer
 * IEEE P1622 Vice Chair
 * [Center for Election Science](https://electionscience.org/) Board member
 * Software developer
 * Consultant

* History, Links:
 * [The Colorado Risk-Limiting Audit Project (CORLA)](http://bcn.boulder.co.us/~neal/elections/corla/)
 * Pilot audits: early and often

---
## Best Practice: Ballot-Level RLAs

* With a good systems, processes and data, you can do **ballot-level** risk-limiting audits
 which **limit the risk** that tabulation errors or attacks result in getting the wrong outcome

    * In **hundreds** of contests, dozens of counties
    * Across **overlapping districts** in a state
    * **Efficiently**: audited less than ten thousand ballots statewide

* Simultaneously, opportunistically, gather evidence on and report risk levels for **all** the rest of the contests (2018 still work in progress)

* Colorado's new statewide system is among the most **cost effective** and best for auditing: central-count scanners with BMDs available for accessibility

---
## Resources Available

* Four vendors presented and piloted systems that could do ballot-level comparison RLAs in 2015: **central count scanning** systems from **Dominion, Hart, ClearBallot, ES&S**

* **Open source** [ColoradoRLA]() code available to support these audits, continues to be enhanced

---
## Support for RLAs

* Widespread, transpartisan consensus on need for both paper ballots and audits.
 * **2003** Four-party consensus in Boulder Colorado
 * 2017 EAC/NIST Voluntary Voting System Guidelines (VVSG) 2.0
 * 2018 [Securing the Vote: Protecting American Democracy | The National Academies Press](https://www.nap.edu/catalog/25120/securing-the-vote-protecting-american-democracy)

* Huge steps forward, still much to do

* Why is it taking so long to adopt robust audits?
  * Elections are increasingly complicated
  * You can't easily audit the data you've got
  * You can't easily get the data you need
 * Critical _Common Data Standards_ work by EAC / NIST

---
## Common Data Formats

* We need format standards!  EAC/NIST
 * [John Wack: Overview of VVSG-Interoperability Common Data Formats](https://www.eac.gov/events/2017/09/11/tgdc-meeting-september-11-12-2017/) (two presentations)

* Election Results CDF V1 published as SP 1500-100.
 * Used in OH, NC, LA County, other states in progress.
* V2 synchronizes with Google/VIP 5.1, adds JSON.
* Election Log Export CDF soon published as SP 1500-101.
* Voter Records Interchange CDF slated for review by VR vendors and then published as SP 1500-102.
 * Initial use in OH and by OSET.
* Cast Vote Records CDF schema to be published as SP 1500-103.
* Continued development and documentation of election process business models and voting method descriptions.

---
## Evidence presented and checked

* [Public RLA Oversight Protocol](http://bcn.boulder.co.us/~neal/elections/PublicRLAOversightProtocol.pdf), Stephanie Singer, Neal McBurnett 2017

* Elements:
 * 1 Chain of Custody
 * 2 Tabulation
 * 3 Manifest
 * 4 Commitment
 * 5 Random selection
 * 6 Ballot card retrieval
 * 7 Ballot Interpretation and data entry
 * 8 Ending the random selection and examination of ballots cards
 * 9 Hand Count
 * 10 Audit Conclusions Affect Outcomes

---
### Convincing Officials of Election Outcomes

* ColoradoRLA includes `rla_export` tool to provide necessary data for Oversight Protocol in csv/json formats

* `rla_report` demonstration code in progress to precisely explain and implement oversight steps.

* Verifiers should of course implement or vet their own processes, code, etc.

* Level 1: Election Adminstrators
 * Colorado counties and state, based on _their_ knowledge of the CVRs etc, dramatically limited the risk of an incorrect tabulation outcome in *hundreds* of contests

Far more than most states can say, very efficient!

---
### Convincing Others of Election Outcomes

* Levels 2 and 3: Losers and the Public
 * Much more transparency than in the past
 * Still several crucial holes left in oversight protocol
 * Some summary data not available yet
 * Wrestling with ballot anonymity issues => no CVRs
     * Can't check totals, interpretations, etc.

 * Nevertheless, appreciate amazing ongoing accomplishments by state and counties under very challenging circumstances!
 * More to come!

???
* Precedent

Has been done

big lift in Boulder in 2008 to generate auditable data, I designed and enabled the audit, wrote software, shoutout to clerk Hillary Hall and her staff for stepping up to it and taking it over for several years.
passed laws

first dice ceremony in 2008.
released all the data to be audited
random selection of contests, then of ballots for each contest.
40000 votes audited.  [calculate nominal risk level]

---
## Discrepancy Investigations

* Detailed reports still in-progress

* Software should inform Audit Board of each discrepancy right after entry.
 That would help investigation, quality control feedback, and trust in the process.

* Poorvi Vora and I have a document in progress on how to investigate discrepancies, preserving integrity, efficiency, flexibility
* More data would be invaluable in fine tuning the process

---
## Remaining Challenges 1

* Enhance reporting convenience and analysis
 * Discrepancies, risk levels for opportunistically audited contests in arbitrary mix of counties
 * Automatic generation, publication of Audit Center for public

* Modularize software for use with external statistical modules, additional methods (SUITE, Bayesian, etc.)

* Handle In-Precinct/Vote center scanners, which randomize ballots and/or CVRs: complicate process of matching paper ballot with CVR

* Support batch-comparison audits (generally predictable risk reduction), ballot-polling audits (unpredictable, impractical for tight margins)

---
## Remaining Challenges 2

* Foster collaboration between clerks, privacy experts, toolsmiths around preserving anonymity, especially for complicated situation in Colorado

* Audit more systems: VR, signature verification, envelope sorters

???

## TODO

get slides from Hilary

what is format - 4:3?  test them

---
## Targeted audits

* Encourage candidates, public to identify additional interesting ballots to target for auditing
 * In addition to full random selection audit
* Could be chosen based on CVRs, mark density data, ballot images

---
## Public engagement in verification

* Promote public participation in audit
* Print ballot tracking pages with QR codes 
* App to photograph ballot + QR code
* Assist public tweets like "I verified this vote"

---
## Acknowlegements

* Paul Tiger
* Joe Pezzillo
* Paul Walmsley
* Ron Rivest
* Philip Stark
* Harvie Branscomb
* Hillary Hall and Boulder County team
* Election Verification Network
* Colorado Legislators
* Incredible dedication of SOS staff and Clerks!
* Free & Fair Team beyond the call of duty
* Galois support

Updated slides:  
 [http://bcn.boulder.co.us/~neal/elections/audit-summit.pdf](http://bcn.boulder.co.us/~neal/elections/audit-summit.pdf)
