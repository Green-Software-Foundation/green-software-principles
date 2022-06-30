# Measuring Software

What you can't measure, you can't improve

<!-- 
## Learning Objectives

* What are the challenges with calculating carbon emissions for software using the GHG protocol? (open-source/doesn't factor growth/attributional not consequential/emissions fall into different scopes depending on software type/organizational not software boundaries) [Evaluation]
* What is the SCI [Knowledge]
* What are the components of the SCI equation [Comprehension]
* How might you quantify an SCI score for an open-source library which has no data regarding where it's used [Application]
* How might you quantify an SCI score for a cloud application where you have data regarding where it's used. [Application]
* _~~List 3 methods for quantifying the energy consumption of a process (direct hardware measurement, software measurement, modeling via utilization) [Comprehension]~~_
* _~~Your Application had an average utilization of 23% and ran for 56hrs. How might you choose to calculate E in your SCI calculation? [Synthesis]~~_
* _~~You used this example server for 56 hrs. What is the value of M you would use in your SCI calculation? [Synthesis]~~_
* Can you list the step-by-step process quantifying an SCI score? [Comprehension]
* Can you complete this example SCI calculation? [Synthesis]
* Given this SCI calculation, would you focus more on energy efficiency or on reducing the amount of hardware the Application uses? [Synthesis]

--> 

## Measuring software using the Greenhouse Gas protocol

The Greenhouse Gas (GHG) protocol is the most common method organizations use to measure their carbon emissions.

### What scope does my application fall in?

The GHG protocol asks us to bucket software emissions according to Scope1, 2, and 3. When it comes to software this presents some interesting challenges.

Most organizations have many applications, all running with different architectures and in different environments.

For the cloud applications running on servers that you own, then the energy usage of your software falls into scope 2, and the embodied carbon of all your servers falls under scope 3.

For the cloud applications running on a public cloud, the energy usage of your application falls into scope 3 as well as the embodied carbon.

In scenarios where you are running a hybrid private/public cloud application, part of its emissions from energy will fall into your organization's scope 2, and part will fall into scope 3.

Similarly, for your customer facing front end application the energy usage falls into your organization's scope 3 since your customer will be purchasing the energy to power their device.

For software, regardless of whether it's run on infrastructure you own, rent, or consumers own, only three emissions categories are important to software teams. How much energy it consumes, how clean or dirty that electricity is, and how much hardware it needs to function. Those are the three categories where it's helpful to bucket emissions from the software perspective.

### Is it possible to calculate a total for software carbon emissions?

To calculate a total for software carbon emissions, you need access to detailed data regarding the energy consumption, the carbon intensity, and the hardware your software is running on. This is challenging data to gather, even for an organization's own closed source software products where they can track its usage with telemetry or logs. Open-source software maintainers don't have the same visibility into how and where their software is used, how much energy is consumed and on what hardware.

Open source projects typically have multiple contributors from multiple organizations. As a result, the responsibility of calculating the emissions is not clear, and neither is it clear who is accountable for eliminating emissions. When you also consider that open source software makes up 90% of a typical enterprise stack, that's a large amount of carbon emissions not accounted for.

### Do totals tell the whole story?

A total is only one metric that describes the state of something. To make the right decisions, we have many different metrics. 

Imagine a scenario where you are the leader of an organization and charged with reducing the emissions of your software. You take steps to measure the total emissions in Q1 as 34 tonnes. You made some investments into projects that eliminate emissions, and by Q2, the emissions have **increased** to 45 tonnes. Should you continue your investments in those projects or cancel them? Should you be fired or promoted?

A total all by itself doesn't tell the whole story. We need other metrics to help describe what's going on. For example, if we looked at the carbon intensity as well as the carbon total, we might see another perspective on what happened. Your software product might have had a carbon intensity of 3.3g CO<sub>2</sub>eq/User in Q1, and in Q2, this **reduced** to 2.9g CO<sub>2</sub>eq/User.

The total informed you that your organization's carbon emissions had increased overall and that might inform one set of decisions. The intensity informed you that your choices to eliminate emissions are working. It would be best to continue in that direction to gain even further reductions.

## Software Carbon Intensity Specification

The [Software Carbon Intensity (SCI) Specification](https://grnsft.org/sci) is a methodology developed by the Standards WG in the Green Software Foundation designed to score a software application along a dimension of sustainability and designed from the ground up to bias action towards **eliminating emissions**.

It’s not a replacement for the GHG protocol, it’s another type of metric that helps software teams understand how their software behaves with respect to carbon emissions so they can make more informed decisions.

Instead of bucketing the carbon emissions of software into scopes 1, 2, and 3, it buckets them into operational emissions (carbon emissions from the running of software) and embodied emissions (carbon emissions from the physical resources required to run the software). It’s also an intensity rather than a total, which amongst other advantages opens the door to open-source software.

The full specification is available at [https://grnsft.org/sci](https://grnsft.org/sci).

### Applicability

The SCI is a method of scoring any software application. Not just cloud and not just end-user applications, but all types of applications in between. It provides a common language to describe how software behaves with respect to carbon emissions as well as how a proposed change might eliminate some of the emissions.

### Equation

The equation to calculate an SCI score is elegantly simple. The elegance allows it to be easily understood and applicable in a wide range of scenarios.

`SCI = ((E *I) * M) per R`

Where:

`E` = Energy consumed by a software system

`I` = Location-based marginal carbon emissions

`M` = Embodied emissions of a software system.

`R` = Functional unit (e.g. carbon per additional user, API-call, ML job, etc)

This summarizes to:

`SCI = C per R`

Carbon per `R`.

`R` is the core characteristic of the SCI and turns it into an intensity rather than a total. This is what we call a Functional Unit. We recommend selecting the Functional Unit that best describes how your application scales. If your application scales by the number of Users, then pick Users as a starting point.

You may calculate multiple SCI scores for the same application. The SCI score is helpful information to understand how your application behaves with respect to carbon emissions in different scenarios. For example, a streaming application might choose Carbon per Minute. It might also calculate a Carbon per User per Day. Maybe Carbon per $ revenue might give another helpful dimension.

### How does the SCI encourage investment into the three pillars of green software?

If you make your application more energy-efficient, hardware efficient, or carbon aware, your SCI score will decrease. There are no shortcuts; the only way to reduce your SCI score is to invest time or resources into one of those three principles.

Adopting the SCI as a metric for your software application will drive investment into one of the three pillars of green software, energy efficiency, hardware efficiency, and carbon awareness.

### Why don’t offsets reduce an SCI score?

Purchasing offsets in the form of neutralizations, compensations, or offsetting electricity in the form of renewable energy credits do **not** reduce your SCI score.

To understand the reasoning for this decision, let's imagine two cloud applications, applications A and B. Team A has invested significant time and resources into making sure application A is using resources efficiently. Team B has made no such investments, and application B uses resources very inefficiently. Therefore, for the SCI to be a helpful metric, application A **needs to score lower** than application B.

If offsets were included in the SCI score and both applications were running on a cloud platform that is 100% carbon offset and matched 100% by renewable energy, **both their SCI scores would be 0**. The SCI score would then essentially provide no helpful information.

Application A which has had significant investment into efficiency scores the same as application B, where the team has invested nothing into efficiency.

Application A emits fewer carbon molecules into the atmosphere. Application B emits more carbon molecules. Since both applications score 0 and the lowest score is 0, why would either team, especially team B, make further investments in improving the carbon efficiency?

### How does the SCI help an organization meet its Net-Zero commitment?

The SCI is a metric specifically designed to drive the elimination of emissions. It's a score, lower numbers are better than higher numbers, and reaching zero is impossible. The only way to reduce your score is to invest time and resources into actions that eliminate emissions. The only activities the SCI recognizes as elimination actions are making your application more energy-efficient, more hardware efficient, or consuming lower-carbon energy sources. Offsets are an essential component of any climate strategy; however, offsets are not eliminations and therefore are not included in the SCI metric.

Any net-zero strategy needs to have plans for how to both eliminate as well as neutralize emissions. The SCI helps organizations drive the elimination of emissions due to software. This makes the SCI an essential component of any net-zero strategy.

### Methodology

Calculating your SCI score requires several steps.

#### What

What software components to include or exclude in the SCI score. This defines your software boundary, where does it start, and where does it end.

For every software component included, you will need to measure its impact. For every major component you choose to exclude, you need to explain why.

The SCI specification doesn't currently make any demands regarding what to include and what not to include; however, you must include all supporting infrastructure and systems that significantly contribute to the software operation.

Your SCI score might decrease because you tightened your software boundary and excluded more software components. Conversely, your SCI score might increase because you are including software components you previously excluded. Therefore, when you report your SCI score, especially any improvements in the score, it's essential to disclose your software boundary.

#### Scale

The SCI is a rate. Carbon emissions per one functional unit. The next step is to pick the functional unit which best describes how your application scales.

The specification currently doesn't prescribe the Functional unit. You are free to pick whichever best describes how your application scales. Future iterations of the SCI might prescribe specific Functional Units for different types of applications to aid with comparability. For instance, we might ask streaming applications to choose a Functional Unit of "Minute" since Carbon per Minute would seem to be a standard method of measuring across all streaming applications.

#### How

Now you have a list of the software components and the functional unit. The next step is to decide how you will quantify the emissions of each software component.

There are two methods of quantification, measurement, and calculation.

Measurement is using counters of some form, for example, measuring the energy consumption of your software component by using a hardware device in the wall socket. Or using counters on hardware that directly measure energy consumption. If you are directly counting something, this is the measurement approach.

Calculation involves indirect counting, often using a model of some form. For instance, if you cannot directly measure your application's energy consumption but instead have a model that estimates the energy consumption based on the CPU utilization, this is considered calculation rather than measurement.

Understanding what to do here is challenging. However, there are two places where you can find help:

* Look at existing case studies in the Software Carbon Intensity Specification. See how others have chosen to measure similar software components with similar context to you.
* Look at the Software Carbon Intensity Data project. This project is responsible for providing advice regarding how to quantify the emissions of different software components.

#### Quantify

This is the execution phase. Using the method described in the how step, execute the method to quantify the SCI score for each software component in your boundary.

The total SCI score of your software application is the sum total of the SCI scores of every software component.

## Summary

A [metric](https://dictionary.cambridge.org/dictionary/english/metric) is a system for measuring something. A metric should help you make decisions. If a metric doesn't help you make decisions, then why calculate it? For example, the GHG Protocol is a metric for measuring an organization's carbon emissions, and it helps organizations make decisions. The SCI is one of many metrics teams can use to help make decisions concerning software.

The SCI is carefully designed, so eliminating emissions is the only way to reduce the score. Together with a separate neutralization strategy, it can form the basis of a net-zero strategy for an organization.

The SCI is very suitable for open-source software where it's often impossible to calculate totals since you cannot know to what extent your software is used.
