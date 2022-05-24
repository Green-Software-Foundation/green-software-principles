# Hardware Efficiency

Use the least amount of embodied carbon possible.

<!-- ## Learning Objectives

### Embodied Carbon 
* What is embodied carbon? [Knowledge]
* What accounts for the total carbon pollution of a computer? [Knowledge]
* Can you describe a scenario where embodied carbon is a significant contributor to the total emitted carbon of hardware? [Comprehension]
* Can you explain how hardware can be thought of as a proxy for carbon? [Comprehension]
* Can you list at least 1 technique where you can be more efficient with hardware? [Knowledge]
* Can you explain how hardware efficiency can affect carbon pollution? [Comprehension]
* What is amortised carbon of a device? [Knowledge]
* Can you describe a scenario whereby the amortised carbon can decrease by extending the lifespan of hardware? [Comprehension]
* What is public cloud? [Knowledge]
* What is private cloud? [Knowledge]
* What would you do to reduce embodied carbon of hardware when using a public cloud provider? [Application]
* What would you do to reduce embodied carbon of hardware in an on-premises data centre (a.k.a private cloud) setup? [Application]
* Can you explain why embodied carbon is considered more significant than the carbon emitted during executions (i.e. electricity drawn when running software)? [Comprehension] -->

## Introduction

The device we are reading this document on released some carbon during its creation. Once it reaches the end of life, disposing of it may release more. Embodied carbon (otherwise referred to as "Embedded Carbon") is the amount of carbon pollution emitted during the creation and disposal of a device. When calculating the total carbon pollution for the computers running software, account for both the carbon pollution to run the computer and the embodied carbon of the computer.

<Image Idea- https://greensoftware.foundation/articles/sustainable-systems-user-hardware-and-sustainability>

Embodied carbon varies drastically between end-user devices. For some devices, the carbon emitted during the manufacturing phase outstrips what is emitted during usage, highlighting that the embodied carbon cost can be much higher than the carbon cost of the electricity powering it.

For example, a desktop computer is estimated to emit 132 kg CO2eq/year, where XX kg CO2eq/year for production, during XX kg CO2eq/yea for the actual electricity usage. In the contrary, a mobile phone is estimated to emit 8 kg CO2eq/year, where XX kg CO2eq/year for production, during XX kg CO2eq/yea for energy usage.

By thinking of embodied carbon, any device, even one not consuming electricity, effectively releases carbon over its lifetime.

## Don't waste hardware

By the time we buy a computer, it's already emitted much carbon. Computers also have an expiry date, and they get old, can no longer handle modern workloads, and need to be refreshed. If we think about it this way, hardware is then a proxy for carbon, so as Green Software Engineers, we must be hardware-efficient if our goal is to be carbon-efficient.

We can do many things to be hardware efficient, but one thing we can do is help extend the expiry date on hardware. Computers don't usually wear out; they become obsolete because we continually create software that pushes limits.

## Extending the lifespan of hardware

A way to account for embodied carbon is to amortise the carbon over the expected life span of a device. For example, if it took 4 tons of carbon to build a server and we hope the server has a 4-year lifespan, we can consider this equivalent to releasing 1 ton of carbon every year. 

If we add one more year to the lifespan of our 2019 R640 Dell Server, then the amortised carbon drops from 320kg CO2eq/year to 256 kg CO2eq/year.

Hardware is retired either because it breaks down or struggles to handle modern workloads. The software cannot help with the first. However, if we focus on building applications that can run on older hardware, we can help with the second. Many factors decide whether a cloud infrastructure is a correct fit in today's computing world. Contrarily, there are many use cases where cloud computing is not the right fit (yet). 

## Public Cloud v.s. Private Cloud
<Image Idea- https://cf-assets.www.cloudflare.com/slt3lc6tev37/2jBaVWKgbOUNLDNw7QJYPh/563316b4290e2919f7510ae59a3ae3ca/public-cloud-vs-private-cloud.svg>
In a public cloud, a third-party provider owns and manages infrastructure such as hardware, storage, and network devices, where multiple customers share the cloud resources and receive the services over the internet. A private cloud- sometimes referred to as an on-premise data centre, is owned by a single organisation and infrastructure is not shared with others. 

Choosing to deploy workload in a public cloud allows users to optimise their workload while striving for maximum utilisation. Additionally, the users are sharing the embodied carbon of infrastructure. This is a significant point to consider when choosing between public and private clouds. We can think of the public cloud as a bus and the private cloud as a car, where carbon pollution associated with using a bus is shared between multiple passengers while the latter is not shared.


## Summary

This section reiterates an essential tale for Green Software Engineer to look beyond direct emissions (Scope 1) of running software. The focus on delivering greener software while deploying workload to a public cloud is to right-size and increase utilisations. For a none public-cloud environment, the focus on building greener software shifts to preserving hardware for as long as possible.

Reference
* https://principles.green/principles/embodied-carbon/
* https://blogs.microsoft.com/blog/2020/01/16/microsoft-will-be-carbon-negative-by-2030/
* https://www.boavizta.org/en/blog/empreinte-de-la-fabrication-d-un-serveur 
