# Energy Efficiency

Use the least amount of energy possible.

<!-- ## Learning Objectives

### Electricity
* What is Electricity? [Knowledge]
* What is Energy? [Knowledge]
* How is energy related to electricity? [Knowledge]
* What are fossil fuels? [Knowledge]
* What is clean energy? [Knowledge]
* What are some of the methods to measure the energy consumption of an application [Knowledge]
* What is PUE (Power Usage Effectiveness)? [Knowledge]
* How would you compare and contrast PUE for an application running in DC and running in non*DC [Application]?
* How would you summarise the energy consumption of a computer? [Comprehension]

### Energy Proportionality
* What is energy proportionality? [Knowledge]
* What is sever utilisation? [Knowledge]
* How can you model energy consumption based on utilisation? [Application]
* What is proportionality (mathematically speaking)? [Knowledge]
* What is the relationship between power and utilisation? [Knowledge]
* What is hardware efficiency? [Knowledge]
* What is static power draw? [Knowledge]
* What is the most efficient and green approach to run a workload? [Comprehension] -->

## Introduction

Most people think electricity is clean. When we plug something into a wall, our hands don't become dirty, and our laptops don't need exhaust pipes. However, the truth is that most electricity is produced through burning fossil fuels — [usually coal](https://ourworldindata.org/grapher/world-electricity-by-source) — and energy supply is the [single most significant](https://www.eea.europa.eu/data-and-maps/daviz/change-of-co2-eq-emissions-2#tab-chart_4) source of carbon emission.

Since we can draw a direct line from electricity to carbon emissions, electricity can be considered one of the proxies for carbon.

All software, from the applications running on mobile phones to the training of machine learning models running in data centres, consumes electricity. One of the best ways to reduce electricity consumption and the subsequent emissions of carbon pollution made by software is to make applications more energy-efficient.

The software creators often do not have to bear the burden of their software's electricity, which economists call an externality, i.e. someone else's problem. Green software takes responsibility for its electricity and is architected to consume as little as possible.

## Energy

Energy is the ability to do work. There are many different forms of energy, such as heat, electrical and chemical. We can convert energy from one form to another. For example, we convert chemical energy stored in coal into electrical energy. In other words, electricity is secondary energy converted from another energy type. We can think of energy as a measure of the electricity used. The standard unit for energy is Joules (J), while the standard unit to measure energy consumption is kilowatt hours (kWh). We will use kWh throughout the rest of this document. 

## Electricity

Most electricity is still produced by burning fossil fuels. Fossil fuels are decomposing plants and animals containing carbon and hydrogen found in the Earth's crust, for instance, coal, oil, and natural gas. Clean energy comes from renewable, zero-emission sources that do not pollute the atmosphere when extracted. There are overlaps between clean, green and renewable energy. Here's how we can differentiate between them:
* Clean energy = clean air
* Green energy = sources from nature
* Renewable energy = recyclable sources

## Power usage effectiveness

The data center industry uses power usage effectiveness (PUE), developed by Green Grid in 2006, to measure data center energy efficiency. Specifically, PUE measures how much energy the computing equipment uses in contrast to cooling and other overhead supporting the equipment. Computing accounts for nearly all consumed energy when a data center's PUE is close to 1.0. When PUE is 2.0, an additional watt of power is required to cool and distribute power to the IT equipment for every watt used in computing.

Another way to think of PUE is as a multiplier to your application energy consumption to get the actual consumption from the grid. So, for example, if your application consumed 10 kWh and the PUE of the data center where it is running is 1.5, then the actual consumption from the grid is 15 kWh, 5kWh goes towards the operational overhead of the data center, and 10 kWh goes to the servers that are running your application.

## Energy proportionality

Energy proportionality measures the relationship between power consumed by a computer and the rate at which useful work is done (its utilisation).

Utilisation measures how much of a computer's resources are used, usually given as a percentage. A fully utilised computer running at its maximum capacity has a high percentage, while an idle computer with no work to do has a lower percentage. 

The relationship between power and utilisation is not proportional. Mathematically speaking, proportionality between two variables means their rations are equivalent. At 0% utilisation, a computer might draw 100W; at 50%, it might draw 180W; and at 100%, it might draw 200W. The relationship between power consumption and utilisation is not linear and does not cross the origin.

Because of this, the more we utilise a computer, the more efficient a computer becomes at converting electricity to practical computing operations. One way to improve hardware efficiency is to run the workload on as few servers as possible, with the servers running at the highest utilisation rate, maximising energy efficiency.

### Static power draw

An idle computer draws electricity even at zero percentage utilisation. 
This is the static power draw of a computer. The static power draw varies by configuration and hardware components, but all parts have some static power draw. This is one of the reasons that PCs, laptops, and end-user devices have power-saving modes. If the device is idle, it will eventually trigger a hibernation mode and put the disk and screen to sleep or even change the CPU's frequency. These power-saving modes save on electricity, but they have other trade-offs, such as a slower restart when the device wakes up.

Servers are usually not configured for aggressive or even minimal power-saving. Many use-cases running on servers demand total capacity as quickly as possible because the server needs to respond to rapidly changing demands, which lead to many servers in idle modes during low demand periods. An idle server costs carbon from the embodied carbon and its inefficient utilisation.

## Summary

Electricity is a proxy for carbon, so building an application that is energy-efficient is equivalent to building an application that is carbon-efficient.

Green software takes responsibility for its electricity consumption and is designed to consume as little as possible. Quantifying the energy consumption of an application is a step in the correct direction to start thinking about how an application can operate more efficiently. Understanding your application's energy consumption is not the only story. The hardware your software is running on uses some of the electricity for operational overhead. This is referred to as Power Usage Efficiency (PUE) in the cloud space. The concept of energy proportionality adds another dimension of complexity since hardware becomes more efficient at turning electricity into useful operations the more it's used. Understanding all this gives green software practitioners a better understanding of how their application behaves with respect to energy consumption in the real world.
