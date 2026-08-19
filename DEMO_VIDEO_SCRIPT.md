# 3–4 Minute Demo Video Script

## 0:00–0:20 — Introduction

Hello, my name is Onyedikachi Onwuka, and this is my App Feature A/B Test Analysis project.

The project investigates whether a lightweight, low-data landing page could improve conversion and user experience for a mobile-first product under Nigerian network conditions.

This project uses a controlled experimental simulation calibrated with Nigerian telecom network benchmarks.

## 0:20–0:55 — Business Problem and Experiment Design

The business question is: does reducing landing-page weight improve conversion and mobile user experience?

Variant A is the standard landing page, while Variant B is the lightweight landing page.

Conversion rate is the primary KPI. Secondary KPIs include page-load time, data usage, bounce rate, CTA click-through rate and page size.

The statistical significance level is five percent, and I use a two-proportion Z-test with a 95 percent confidence interval.

## 0:55–1:25 — Dataset and Nigerian Context

The dataset contains simulated user-level observations. I validated the data for missing values, duplicate users, experimental groups and binary outcomes before analysis.

The Nigerian context comes from telecom network-performance benchmarks such as download speed, latency, Time to First Byte and packet loss.

An important limitation is that these are benchmark inputs and the individual user outcomes are simulated. Therefore, this is not presented as a live test of Nigerian customers.

## 1:25–2:05 — Primary KPI

The primary metric is conversion rate.

In the simulation, the standard experience produced a conversion rate of approximately 9.23 percent, while the lightweight experience produced approximately 10.71 percent.

That represents an absolute uplift of about 1.47 percentage points and a relative uplift of about 15.95 percent.

This suggests a potentially meaningful business improvement, but I still need to determine whether the difference is statistically significant.

## 2:05–2:45 — Hypothesis Test and Confidence Interval

The null hypothesis states that the conversion rates are equal. The alternative hypothesis states that the lightweight variant has a higher conversion rate.

The two-proportion Z-test produced a Z-statistic of approximately 3.47 and a p-value of approximately 0.00026.

Because the p-value is below 0.05, I reject the null hypothesis in this simulation.

The 95 percent confidence interval for the difference, calculated as Variant B minus Variant A, is approximately 0.64 to 2.30 percentage points.

Because the interval is entirely above zero, it supports a positive treatment effect under the simulation assumptions.

## 2:45–3:20 — Secondary Metrics

I also examined the user-experience metrics.

The lightweight experience reduced average page-load time from about 2.04 seconds to 1.35 seconds, and reduced average data usage from about 2.62 megabytes to 0.82 megabytes.

Bounce rate also fell from approximately 34.42 percent to 25.80 percent, while CTA click-through rate increased from approximately 20.89 percent to 24.22 percent.

These results are directionally consistent with the business hypothesis that a lighter mobile experience can improve usability.

## 3:20–3:50 — Recommendation and Limitations

My recommendation is to treat the lightweight design as the stronger candidate for a follow-up live experiment.

However, I would not claim that these results prove what Nigerian customers will do in production because the user-level observations are simulated.

A live randomized experiment should be the next step, capturing real users, devices, operators, network conditions, performance metrics and conversions.

Thank you for reviewing my App Feature A/B Test Analysis project.
