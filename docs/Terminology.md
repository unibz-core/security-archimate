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

**Examples:** Antivirus software has *Control Capabilities* to scan and eliminate malware. Air defense systems have *Control Capabilities* to intercept certain air threats. Warning signs have *Control Capabilities* to dissuade people from doing certain things.

<!-- <img src="image.png" width="200" height="100"> -->


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

> A *Likelihood* assignment describes the chances of occurrence of certain types of events or the chances of events to cause (or be followed by) other events.

In ArchiMate, *Likelihood* is represented by an *Assessment* with the stereotype «Likelihood», which can be connected to an event or the triggering association between events. Since there is no sense in assigning likelihood to individual events, the likelihood assignment should be understood as describing regularities, so applicable to types of events.

Events that prevent others from happening can be understood as negatively influencing the likelihood of the occurrence of the latter.

**Examples:** 20% likelihood of data breaches. 30% likelihood of vulnerability exploitation causing data breaches.

<!-- TOC --><a name="loss-event"></a>
### 9. Loss Event

> *Loss Events* are events that compromise (negatively impact) stakeholders' goals.

In ArchiMate, *Loss Events* are events stereotyped with «LossEvent». There is a negative *influences* association between a *Loss Event* and a *Goal* of a given Agent (a *Risk Subject*), which captures why an event is considered a loss. Loss events are caused (triggered) by *Threat Events*.

**Examples:** Production loss event hurts the Business owner's goal of maximizing production.

<!-- TOC --><a name="object-at-risk"></a>
### 10. Object at Risk

> The asset or resource at stake, i.e., the thing that may be harmed or damaged in a *Loss Event*.

In ArchiMate, an *Object at Risk* is represented by a Structure Element stereotyped with «AssetAtRisk».

In the risk ontology, we distinguish two roles played by objects in a *Risk Experience*, namely the OBJECT AT RISK and the *Threat Enabler*. In both cases, the dispositions of these objects enable the occurrence of threat and *Loss Events*. The difference between them is that the former is the thing at stake (i.e., the thing that may be harmed or damaged in a *Loss Event*), whilst the latter is simply a risk-enabling thing, as it is not exposed to any potential damage.


**Examples:** To exemplify this distinction between an *Object at Risk* and a *Threat Enabler*, consider that a machine failed and caused a production loss. It was the machine’s vulnerability that caused it to fail. Still, the integrity of the machine might not be affected by the failure at all. In this case, the machine is playing the role of a *Threat Enabler*.

<!-- TOC --><a name="protected-subject"></a>
### 11. Protected Subject

> An agent whose goals are protected by the effects (*Control (Protection) Events*) of a *Security Mechanism*.

This protection effect is the prevention of *Risk Events* (*Threat* or *Loss Events*) that could hurt the agent's goals.

In ArchiMate, a *Protected Subject* is represented by a specialization of *Risk Subject* associated with a «ControlObjective»

The *Protected Subject* specializes *Risk Subject*, though some *Risk Subjects* might not be *Protected Subject* due to lack of protection.

**Examples:** For example, a company has a *Control Objective* of protecting customers’ data from cyberattacks. Based on an assessment, a series of *Control Measures* should be implemented by the company’s cybersecurity team, playing the role of *Security Designer*; both the company and the customers may be regarded as *Protected Subjects* since they have assets at risk that should be protected.

<!-- TOC --><a name="protection-trigger"></a>
### 12. Protection Trigger

> Certain state of affairs or environmental conditions that activate *Control Capabilities*.

In ArchiMate, a *Protection Trigger* is represented as an *Assessment* stereotyped with «ControlAssessment».

The advantage of explicitly accounting for the situations that trigger the *Protection (Control) Event* is that we can represent how several environmental factors increase the effectiveness of the *Security Mechanism*, assuming its effectiveness is directly connected to how likely it works properly, manifesting the *Protection Event*.

**Examples:** A circuit breaker manifests its capability of interrupting a current flow when a fault condition is detected (heating or magnetic effects of electric current).

<!-- TOC --><a name="quality"></a>
### 13. Quality

> In the Unified Foundational Ontology, a *quality* is an objectification of a property that can be directly evaluated (projected) into certain value spaces.

In ArchiMate, a *quality* is represented as a Driver stereotyped with «Quality». Specific values are assigned through an assessment associated with the «Quality» Driver.

**Examples:** Consider an airplane seat (*Resource*) associated with seat width («Quality» Driver), associated with an assessment 43 cm. Other examples include the weight of a person, which can be measured in kilograms or pounds, and the color of a flower, which can be specified in RGB or HSV.

<!-- TOC --><a name="risk-experience"></a>
### 14. Risk Experience

> Definition...

A second characteristic of use value is that, ultimately, it is ascribed to experiences, not objects. This may sound counter intuitive at first, as we have mentioned several examples of value seemly being attributed to objects. To clarify this point, let us go back to the winter jacket example. To ascribe some value to a jacket, we need to consider the situations in which we envision ourselves using such a jacket. It could be a snowy day while we go to work, a winter hike on the Italian Dolomites, or a rainy evening when we go to a dinner. In each of these situations, we will have different goals that we expect the jacket to help us fulfill, such as staying warm and dry, looking fashionable, keeping our belongings and so on. The value that we ascribe to the jacket, thus, will be “calculated” from the value ascribed in these envisioned experiences. Despite its subjective nature and the fact that value is ultimately grounded on experiences, value is directly affected by the intrinsic properties of the objects that participate in these experiences. For instance, if a jacket is worn during a hike, it will be more or less valuable depending on its weight (an intrinsic quality that inheres in the jacket), as lighter jackets facilitate exercise. The same analysis holds for a jacket’s waterproof capability on a rainy day: the more it can repel water, the more it satisfies its wearer’s goal of staying dry. By considering the whole experience in which objects are used, we are able to explain that not only intrinsic properties of things affect their value, but also the properties of other objects and of the experience itself. This is useful, for instance, to explain that the value experienced by a user of a movie streaming service is affected by the speed of the internet connection used to access it, as well as the screen resolution of the streaming device.

The experiential perspective is depicted in Figs. 1 and 2. As argued in the previous section, value and risk can be ascribed to both objects and events. Still, whenever they are ascribed to an object, one must always consider all the relevant events involving it, which will ultimately ground value and risk. These events, named VALUE and RISK EXPERIENCE, have some agents as key participants, deemed VALUE and RISK SUBJECT respectively. These identify the perspective from which the judgment is made and whose INTENTIONS are considered.

In ArchiMate, *Risk Experience* is represented as an Grouping element stereotyped with «RiskExperience»

*Risk Experience* aggregates the risk elements and the relations, including *Hazard Assessment*, *Threat Agent*, *Loss Event*, *Vulnerability*, *Asset at Risk*, and *Threat Enabler*.


**Examples:** XXXX.

<!-- TOC --><a name="risk-driver"></a>
### 15. Risk

> Definition...

The second represents risk from a quantitative perspective, commonly described as probability × impact. We map this concept as a DRIVER stereotyped as RISK, as drivers represent “conditions that motivate an organization to define its goals and implement the changes necessary to achieve them”

Associated to this experience, there is RISK simply labeled “Production loss”, which reflects the likelihood that all the parts of the experience occur and cause each other, as well as on the quantitative impact of the potential losses. Lastly, the RISK ASSESSMENT “Risk of production loss is unacceptable” concerns the production loss RISK.

stereotyped with «Risk»


**Examples:** XXXX.

<!-- TOC --><a name="risk-subject"></a>
### 16. Risk Subject

> The agent whose *Intentions* (goals) could be affected by a potential loss.

In ArchiMate, a *Risk Subject* is represented as a Stakeholder associated with a Goal that is negatively impacted by a «LossEvent».

**Examples:** Business owner.

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

> An agent responsible for the introduction of a Security Mechanism.

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
        
