---
title: Terminology
layout: home
---

## Terminology

The terminology of our proposal to introduce notions related to **Risk** and **Security** into ArchiMate language.

<!-- TOC start (generated with https://github.com/derlin/bitdowntoc) -->

- 1\. [Control Capability](#control-capability)
- 2\. [Control Event](#control-event)
- 3\. [Control Measure](#control-measure)
- 4\. [Control Objective](#control-objetive)
- 5\. [Disposition](#disposition)
- 6\. [Hazard Assessment](#hazard-assessment)
- 7\. [Intention](#intention)
- 8\. [Likelihood](#likelihood)
- 9\. [Loss Event](#loss-event)
- 10\. [Object at Risk](#object-at-risk)
- 11\. [Protected Subject](#protected-subject)
- 12\. [Protection Trigger](#protection-trigger)
- 13\. [Quality](#quality)
- 14\. [Risk Experience](#risk-experience)
- 15\. [Risk Driver](#risk-driver)
- 16\. [Risk Subject](#risk-subject)
- 17\. [Risk Assessment](#risk-assessment)
- 18\. [Risk Assessor](#risk-assessor)
- 19\. [Security Designer](#security-designer)
- 20\. [Security Mechanism](#security-mechanism)
- 21\. [Threat Enabler](#threat-enabler)
- 22\. [Threat Event](#threat-event)
- 23\. [Threat Object](#threat-object)
- 24\. [Vulnerability](#vulnerability)

<!-- TOC end -->

<!-- TOC --><a name="control-capability"></a>
### 1. Control Capability

> A *Control Capability* is a capability whose manifestation is a *Control (Protection) Event*.

In ArchiMate, a *Control Capability* is represented by a *Capability* associated with *Control (Protection) Event*.

A *Security Mechanism* aggregates *Control Capabilities*. However, other objects may also have one or more *Control Capabilities*.

**Examples:** Antivirus software has *Control Capabilities* to scan and eliminate malwares. Air defense systems have *Control Capabilities* to intercept certain air threats. Warning signs have *Control Capabilities* to dissuade people from doing certain things.




<!-- TOC --><a name="control-event"></a>
### 2. Control Event

> A *Control Event* (or *Protection Event*) is an event that prevents, directly or indirectly, *Threat Events* or *Loss Events* of a certain type.

In ArchiMate, a *Control Event* is represented by an event that must negatively influence the «Likelihood» associated with events stereotyped with «ThreatEvent» or «Loss Event».

*Control Events*, directly, realize a *Goal* stereotyped with «ControlObjective» or, indirectly, realize it via the realization of a *Requirement* stereotyped with «ControlMeasure», which should realize that *Goal*.


*Control Events* are manifestations of *Control Capabilities* which they are associated with.

**Examples:** To realize the «ControlObjective» *Goal* of preventing software failure, removing permission to commit to the repository can be an adequate *Control Event*. Rocket interception can be a *Control Event* as manifestation of an air defense system's *Control Capabilities*; by doing so, the rocket interception event realizes the «ControlObjective» *Goal* of preventing damage to a given factory.

<!-- TOC --><a name="control-measure"></a>
### 3. Control Measure

> In a risk analysis process, a *Control Measure* is a specification of an action or set of actions that have to be performed or that should be implemented as part of the control, treatment, and mitigation of a particular risk.

In ArchiMate, a *Control Measure* is represented by a *Requirement* with the stereotype «ControlMeasure». A a *Control Measure* is realized by the implementation of a *Security Mechanism* or by a *Control Event*.

**Examples:** Enforcing no-logs policy within a VPN company. Autoupdate feature of a piece of software. Warning signs nearby dangerous places inside a factory.


📝 **Note:** A *Control Measure* is a *Requirement* and, as such, a proposition or statement. It is not a concrete thing. For example, the warning signs above correspond to the proposition regarding employing them; the warning signs themselves can be seen as *Security Mechanism*, placed by an implementation event assigned to a *Security Designer*.

<!-- TOC --><a name="control-objective"></a>
### 4. Control Objective

> A high-level goal that should be realized by one or more *Control Measures*.

In ArchiMate, a *Control Objective* is represented by a *Goal* stereotyped with «ControlObjective». A *Control Objective* is realized by a a *Requirement* stereotyped with «ControlMeasure».

**Examples:** Preventing work accidents. Preventing data breaches. Preventing software failure.

<!-- TOC --><a name="disposition"></a>
### 5. Disposition

> A *Disposition* is a property of being disposed in some specific way. It refers to possible behaviors something may have under certain conditions.

In ArchiMate, a *Disposition* is represented by a *Capability*.  Abilities, capabilities, capacities, tendencies, powers, liabilities, vulnerabilities, and similar terms refer to *Dispositions*, in this sense.

**Examples:** Flamability of a piece of wood. Vulnerability of an employee to fall for a phishing attack. Commit permission.

<!-- TOC --><a name="hazard-assessment"></a>
### 6. Hazard Assessment

> A *Hazard Assessment*, proposed to represent UFO situations that activate *Threat Capabilities*, is an identified state of affairs that increases the likelihood of a *Threat Event* and, consequently, of a *Loss Event*.

In ArchiMate, a *Hazard Assessment* is an assessment stereotyped with «HazardAssessment».


**Examples:** Employees working too many hours. Disorganized work place in a factory. Unclear procedures for emergency.

<!-- TOC --><a name="intention"></a>
### 7. Intention

> An *Intention* is an internal mode of an agent that is committed to the realization of a goal, which is the propositional content of the *Intention*.

In ArchiMate, an *Intention* is represented by a *Goal*.

**Examples:** Hacker's intention to hack a company. Robber's intentions. Competitor's intentions.


<!-- TOC --><a name="likelihood"></a>
### 8. Likelihood

> Definition...

In ArchiMate, Likelihood is represented by an *Assessment* with the stereotype «Likelihood»...

connected to a triggering association between Value Events or to a «ValueExperience»

**Examples:** XXXX.

<!-- TOC --><a name="loss-event"></a>
### 9. Loss Event

> Definition... Risk Events are the manifestations of (threat) capacities, Vulnerabilities, and, sometimes, Intentions that inhere in an Agent; these Events bring about a Situation that hurts the goal of a given Agent (a Risk Subject)

Event stereotyped with «LossEvent»


**Examples:** XXXX.


<!-- TOC --><a name="object-at-risk"></a>
### 10. Object at Risk

> Definition...

In ArchiMate, an *Object at Risk* is represented by a Structure Element stereotyped with «AssetAtRisk».


**Examples:** XXXX.

<!-- TOC --><a name="protected-subject"></a>
### 11. Protected Subject

> Definition...

In ArchiMate, a *Protected Subject* is represented by a specialization of Risk Subject associated with a «ControlObjective»


**Examples:** XXXX.

<!-- TOC --><a name="protection-trigger"></a>
### 12. Protection Trigger

> Definition...

Assessment stereopyed with «ControlAssessment»

**Examples:** XXXX.

<!-- TOC --><a name="quality"></a>
### 13. Quality

> Definition...

«Quality» Driver

**Examples:** XXXX.

<!-- TOC --><a name="risk-experience"></a>
### 14. Risk Experience

> Definition...

Grouping stereotyped with «RiskExperience»


**Examples:** XXXX.

<!-- TOC --><a name="risk-driver"></a>
### 15. Risk Driver

> Definition...

stereotyped with «Risk»


**Examples:** XXXX.

<!-- TOC --><a name="risk-subject"></a>
### 16. Risk Subject

> Definition...

Stakeholder associated with a Goal that is negatively impacted by a «LossEvent»



**Examples:** XXXX.

<!-- TOC --><a name="risk-assessment"></a>
### 17. Risk Assessment

> Definition...

Assessment associated with a «Risk»

**Examples:** XXXX.


<!-- TOC --><a name="risk-assessor"></a>
### 18. Risk Assessor

> Definition...

Stakeholder associated with a Risk Assessment


**Examples:** XXXX.

<!-- TOC --><a name="security-designer"></a>
### 19. Security Designer

> Definition...

Business Role stereotyped with «SecurityDesigner» (normally, it is associated with «ControlMeasure» and assigned to the implementation of a Security Mechanism)


**Examples:** XXXX.

<!-- TOC --><a name="security-mechanism"></a>
### 20. Security Mechanism

> Definition... is an Object that was intentionally designed to create value by protecting certain goals from Risk Events (encompassing Threat Events and Loss Events) in a systematic fashion.

Structure Element (Business Agent, Resource) stereotyped with «SecurityMechanism»


**Examples:** XXXX.

<!-- TOC --><a name="threat-enabler"></a>
### 21. Threat Enabler

> Definition...

Structure Element associated with a «ThreatEvent» or a «LossEvent»

**Examples:** XXXX.

<!-- TOC --><a name="threat-event"></a>
### 22. Threat Event

> Definition...

Event stereotyped with «ThreatEvent»


**Examples:** XXXX.

<!-- TOC --><a name="threat-object"></a>
### 23. Threat Object

> Definition...

 Structure Element stereotyped with «ThreatAgent»


**Examples:** XXXX.

<!-- TOC --><a name="vulnerability"></a>
### 24. Vulnerability

> Definition...

Capability stereotyped with «Vulnerability»


**Examples:** XXXX.
        
