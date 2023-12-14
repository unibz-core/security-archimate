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

    A Control Capability represents a capability whose manifestation is a Control (Protection) Event.

In ArchiMate, a *Control Capability* is *Capability* associated with *Control (Protection) Event*. A *Security Mechanism* holds *Control Capabilities* but other objects may also have one or more *Control Capabilities*.


<!-- TOC --><a name="control-event"></a>
### 2. Control Event

     Definition...

An event that realizes «ControlObjective», and negatively influences the «Likelihood» associated with «ThreatEvent» or «Loss Event»

<!-- TOC --><a name="control-measure"></a>
### 3. Control Measure

    Definition...

<!-- TOC --><a name="control-objective"></a>
### 4. Control Objective

    > Definition...

<!-- TOC --><a name="disposition"></a>
### 5. Disposition

     Definition...

Capability

<!-- TOC --><a name="hazard-assessment"></a>
### 6. Hazard Assessment

     Definition...

Assessment stereotyped with «HazardAssessment»


<!-- TOC --><a name="intention"></a>
### 7. Intention

     Definition...

«QualityGoal» Goal, «FunctionalGoal» Goal, Goal

<!-- TOC --><a name="likelihood"></a>
### 8. Likelihood

     Definition...

«Likelihood» Assessment connected to a triggering association between Value Events or to a «ValueExperience»


<!-- TOC --><a name="loss-event"></a>
### 9. Loss Event

     Definition... Risk Events are the manifestations of (threat) capacities, Vulnerabilities, and, sometimes, Intentions that inhere in an Agent; these Events bring about a Situation that hurts the goal of a given Agent (a Risk Subject)

Event stereotyped with «LossEvent»



<!-- TOC --><a name="object-at-risk"></a>
### 10. Object at Risk

     Definition...

Structure Element stereotyped with «AssetAtRisk»

<!-- TOC --><a name="protected-subject"></a>
### 11. Protected Subject

     Definition...

A specialization of Risk Subject associated with a «ControlObjective»


<!-- TOC --><a name="protection-trigger"></a>
### 12. Protection Trigger

     Definition...

Assessment stereopyed with «ControlAssessment»



<!-- TOC --><a name="quality"></a>
### 13. Quality

     Definition...

«Quality» Driver

<!-- TOC --><a name="risk-experience"></a>
### 14. Risk Experience

     Definition...

Grouping stereotyped with «RiskExperience»

<!-- TOC --><a name="risk-driver"></a>
### 15. Risk Driver

     Definition...

stereotyped with «Risk»


<!-- TOC --><a name="risk-subject"></a>
### 16. Risk Subject

     Definition...

Stakeholder associated with a Goal that is negatively impacted by a «LossEvent»


<!-- TOC --><a name="risk-assessment"></a>
### 17. Risk Assessment

     Definition...

Assessment associated with a «Risk»


<!-- TOC --><a name="risk-assessor"></a>
### 18. Risk Assessor

     Definition...

Stakeholder associated with a Risk Assessment


<!-- TOC --><a name="security-designer"></a>
### 19. Security Designer

     Definition...

Business Role stereotyped with «SecurityDesigner» (normally, it is associated with «ControlMeasure» and assigned to the implementation of a Security Mechanism)


<!-- TOC --><a name="security-mechanism"></a>
### 20. Security Mechanism

     Definition... is an Object that was intentionally designed to create value by protecting certain goals from Risk Events (encompassing Threat Events and Loss Events) in a systematic fashion.

Structure Element (Business Agent, Resource) stereotyped with «SecurityMechanism»


<!-- TOC --><a name="threat-enabler"></a>
### 21. Threat Enabler

     Definition...

Structure Element associated with a «ThreatEvent» or a «LossEvent»



<!-- TOC --><a name="threat-event"></a>
### 22. Threat Event

     Definition...

Event stereotyped with «ThreatEvent»


<!-- TOC --><a name="threat-object"></a>
### 23. Threat Object

     Definition...

 Structure Element stereotyped with «ThreatAgent»

<!-- TOC --><a name="vulnerability"></a>
### 24. Vulnerability

     Definition...

Capability stereotyped with «Vulnerability»

        
