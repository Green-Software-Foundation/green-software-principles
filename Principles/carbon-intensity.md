# Carbon Awareness

Do more when the electricity is cleaner and do less when the electricity is dirtier.

<!-- ## Learning Objectives

### Carbon Intensity

* What is carbon intensity? [Knowledge]
* What is the standard unit of carbon intensity? [Knowledge]
* What two variables affect carbon intensity? [Knowledge]
* Can you draw a diagram to demonstrate how carbon intensity changes over time? [Comprehension]
* How is electricity supply related to demand? [Knowledge]
* What is a marginal power plant? [Knowledge]
* What is marginal carbon intensity? [Knowledge]
* Can you describe a scenario when marginal carbon intensity reaches 0? [Comprehension]
* What is demand shifting? [Knowledge]
* Why would you consider shifting demand for your application? [Knowledge]
* Can you describe a scenario where demand shifting can affect the carbon intensity of electricity for your application? [Comprehension] 

### Demand Shaping

* What is demand shaping? [Knowledge]
* Can you describe a real-world scenario where demand shifting has been used when demand is not enough? [Knowledge]
* What does carbon aware mean? [Knowledge]
* What's the difference between carbon aware and carbon-efficient? [Knowledge]
* Can you list at least 1 data source and one potential tool that you can utilize to build a carbon-aware application? [Knowledge]
* Why is making your application carbon-efficient may not be enough? [Comprehension]
* What types of applications and features would you consider making carbon aware? [Application]
* Can you explain how carbon awareness can help power grids transition towards 100% renewable power? [Comprehension]-->

## Introduction

The carbon intensity of electricity measures how much carbon (CO2eq) is emitted per kilowatt-hour of electricity consumed.

Not all electricity is produced in the same way. In different locations and times, electricity is generated using various sources with varying carbon emissions. Some sources, such as wind, solar, or hydroelectric, are clean, renewable sources that emit little carbon. Other fossil fuel sources emit varying amounts of carbon to produce electricity. For example, gas-burning power plants emit less carbon than coal-burning power plants.

[IMAGE]


## Standard Unit of Measurement

The standard unit of carbon intensity is gCO2eq/kWh or grams of carbon per kilowatt-hour.

If your computer is plugged directly into a wind farm, then its electricity would have a carbon intensity of 0 gCO2eq/kWh since a wind farm emits no carbon to produce that electricity. However, most people can't plug directly into wind farms; instead, they plug into power grids supplied with electricity from various sources. 

Once on a grid, you can't control which sources supply electricity; you are getting a mix of everything. So your carbon intensity will be a mix of all the current power sources in a grid, the lower carbon and the higher carbon sources.


## Variability of Carbon Intensity

**Carbon intensity changes by location** since some regions have an energy mix that contains more clean energy sources than other regions.

[IMAGE]

**Carbon intensity also changes over time** due to the variable nature of renewable energy. For example, when it's cloudy or the wind isn't blowing, carbon intensity increases since more of the electricity in your mix comes from sources that emit carbon.

[IMAGE]


## Balancing Supply and Demand

Electricity demand varies during the day, and that demand needs to be met by supply. If a utility doesn't produce enough electricity to meet demand, there is a brownout. Suppose a utility produces more electricity than is required, then stop infrastructure burning out breakers trip, and we have blackouts. There needs to be a balance between the demand and supply of electricity at every moment. Who has responsibility for this differs between electricity grids, but it's the utility provider for simplicity.


### Dispatchability & Curtailment

Some of that supply can easily control the power it produces, e.g., a coal power plant can burn less coal; this is called **dispatchability**. However, some of that supply can't easily control the power it produces, e.g., a wind farm can't control how much the wind blows. So if it makes more electricity than is currently needed, that electricity is thrown away; this is called **curtailment**.


### Marginal Carbon Intensity

If you choose to consume more energy, that energy comes from the marginal power plant. 

The marginal power plant is dispatchable; it can control the energy it outputs. Renewable plants cannot control the sun or the wind, so marginal power plants are often powered by fossil fuels.

We have the average carbon intensity of all the energy in the grid at any moment. Marginal carbon intensity is the carbon intensity of the power plant that would have to ramp up to meet any new demand. If you were to turn on a light right now, a specific power plant would have to output more energy. So **marginal carbon intensity** is the carbon intensity of that particular power plant.

Fossil-fueled power plants rarely scale down to 0. They have a minimum functioning threshold, and some don't scale at all; they are considered consistent always-on baseload. Because of this, we can sometimes reach the perverse scenario where we curtail (throw away) renewable energy while still consuming energy from fossil fuel power plants.

[IMAGE] 

The marginal carbon intensity will be 0 gCO2eq/kWh in these situations since we know that any new demand will match the renewable energy we are curtailing. 


<!-- ## Calculating Carbon Intensity

Several services allow you to obtain real-time and predicted data regarding the carbon intensity of different electricity grids. Some provide estimates of future carbon intensity, and some provide the marginal carbon intensity.



* Carbon Intensity API: Free resource for carbon intensity data in the UK.
* ElectricityMap: Free for non-commercial single country use, premium solutions for commercial and multi-country access.
* WattTime: Free for a single grid region, premium solutions for multi-grid, and real-time marginal emissions. -->


## How Electricity is Bought and Sold

The exact market model varies around the world but roughly works like so:

[IMAGE]

When the demand for electricity goes down, utilities need to **reduce** the supply to balance supply and demand. Therefore, they have two choices in order of preference:



1. They can buy less energy from fossil fuel plants. Energy from fossil fuel plants is usually the most expensive; coal costs money. This directly translates to burning fewer fossil fuels.
2. Buy less energy from renewable sources. Renewable sources are the cheapest, so they prefer not to do this. If a renewable source doesn't manage to sell all of its electricity, it has to throw the rest of it away; this is called curtailment.

Reducing the amount of electricity consumed in your applications can help decrease the energy's carbon intensity as burning fossil fuels is scaled back first.

[IMAGE]

When the demand for electricity goes up, Utilities need to **increase** the supply to balance supply and demand. Therefore, they have two choices in order of preference:



1. Buy more energy from renewable sources that are **currently** being curtailed. If you are curtailing, it means you have excess energy you could dispatch. Renewable energy is already the cheapest, so curtailed renewable energy will be the cheapest dispatchable energy source. Renewable plants will then sell the energy they would have had to curtail.
2. Buy more energy from fossil fuels plants. Fossil fuels are inherently dispatchable; they can quickly scale up energy production by burning more. However, coal costs money, so this is the least preferred solution.

The above is highly oversimplified. Energy markets are some of the most complex markets in the world. But what's important to understand is that **our goal is to increase investment into lower carbon energy sources, like renewables, and decrease investment into higher carbon sources**, like coal. So the best way to ensure money flows in the direction we need is to make sure you use electricity with the least carbon intensity.


## Energy Transition

There is a global transformation happening right now. All around the world, electricity grids are changing from primarily burning fossil fuels to sourcing energy from renewable sources like wind and solar. This is one of our best hopes for meeting our global reduction targets. The question we need to ask ourselves as Green Software Practitioners is, "how can we help accelerate that transition?"

The primary driver for the transition is economic rather than any sustainability target. Renewables are winning because they are cheaper and getting even cheaper over time. So to help accelerate the transition, we need to make renewable plants more profitable and fossil fuel plants less profitable. The best way to do that is to use more electricity when it's coming from renewable sources and less electricity when it's coming from higher carbon sources.

Carbon intensity is lower when more energy comes from lower-carbon sources and higher when it comes from higher carbon sources. 

> Using electricity when the carbon intensity is low is the best way to ensure investment flows to renewable plants and away from fossil fuel plants.


## Carbon Awareness

The idea of doing more when more energy comes from low carbon sources and doing less when more of the carbon comes from high carbon sources is called **carbon awareness**.


### Demand Shifting

One way to consume electricity with less carbon intensity is to do demand shifting. For example, suppose you can be flexible with when and where you run workloads. In that case, you can choose to consume electricity when the carbon intensity is less and pause when carbon intensity is high. For example, training a machine learning model at a different time or region where the carbon intensity is much lower.

Studies show these actions can result in carbon reductions of 45% to 99% depending on the number of renewables powering the grid.

[LIST OTHER STUDIES]

Demand shifting can be further broken down into spatial and temporal shifting. 


#### Spatial Shifting

Spatial shifting means moving your computation to another physical location, where the current carbon intensity is lower. It might be a region that naturally has lower carbon sources of energy. It might be a region where it happens to be windy or sunny right now.

[IMAGE]


#### Temporal Shifting

If you can't shift your computation spatially to another region, another option you have is to shift to another time. Perhaps later in the day or night when it's sunnier or windier and, therefore, the carbon intensity is lower. This is called temporal demand shifting. We can predict future carbon intensity reasonably well through advances in weather forecasting.

[IMAGE]


### Real-World Case Studies

There are several real-world examples of carbon awareness implemented at scale:


#### Google Carbon Aware Data Centres

Google launched a project to make some of the cloud workloads carbon aware. The details of their methodology are in the paper XXXXX. To summarise, they predicted two things, tomorrow's carbon intensity, and tomorrow's workload. They then shaped large-scale workloads so more would happen when and where the carbon intensity is lowest, but in such a way that they could still handle the expected load. This resulted in X percent reduction in carbon emissions for their initial experiment in this space.


#### Microsoft Carbon Aware Windows

Microsoft announced a project to make Windows Carbon Aware XXX; the initial feature prefers running windows updates when the carbon intensity is lower; however, future versions could move more work to times when the CI is lower. Windows runs on over 10 billion devices worldwide, so the impact of this work is scaled many times over.


## Demand Shaping

Demand shifting is the strategy of moving computation to regions or times when the carbon intensity is lowest. Demand shaping is a similar strategy. However, instead of moving demand to a different region or time, we shape our computation to match the existing supply.

[IMAGE] 



* If carbon intensity is low, increase the demand more in your applications.
* If carbon intensity is high, decrease demand do less in your applications.

Demand shaping carbon-aware applications is all about the supply of carbon. When the carbon cost of running your application becomes high, shape the demand to match the supply of carbon. This can happen automatically, or the user can make a choice.


### Eco-modes / Performance-modes

Eco-modes are often used in everyday life: for instance, in cars or washing machines. When switched on, the performance changes as they consume fewer resources (gas/electricity) to perform the same task. However, it's not cost-free (otherwise, we would always choose eco-modes), so we make trade-offs. Because it's a trade-off, eco-modes are often presented to a user as a choice. The user decides to go with it and accept the compromises.

Software applications can also have eco-modes that, when engaged, change application behavior in potentially two ways:



* Giving users information so they can make informed decisions.
* The application automatically makes more aggressive decisions to reduce carbon emissions.


### Examples

A great example of demand shaping is video conferencing software. Rather than streaming at the highest quality possible at all times, they often shape the demand by reducing the video quality to prioritize audio when the bandwidth is constrained.

Another example is TCP/IP. The transfer speed ramps up in response to how much data can be broadcast over the wire.

A third example is progressive enhancement with the web. The web experience improves depending on the resources and bandwidth available on the end-users device. 


## Summary

Demand shaping is related to a broader concept in sustainability, which is to reduce consumption. We can achieve a lot by becoming more efficient with resources, but we also need to consume less at some point. As Green Software Practitioners to be carbon-aware means perhaps when the carbon intensity is high, we consider canceling it instead of demand shifting compute. Reducing the demands of our application and the expectations of our end users.
