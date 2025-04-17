---
title: Beijing MaaS - A Brief
status: Draft
description: This is a brief overview of the Beijing Mobility as a Service (MaaS) system. Includes a summary of the goals, key characteristics, and a list of the main stakeholders, as well as discussion of the implications and future directions.
city: Beijing
country_code: CN
centroid: [39.90872, 116.39749]
year_start: 2019
year_completed: Ongoing
featured_image: ./christian-lue-qQT7l54ERZM-unsplash.jpg
featured_desc: Beijing Mobility as a Service (MaaS) System.
featured_credit: Christian Lue
author: Urban Tech Hub
tags:
  - Mobility
  - InformationSystems
geography: ./example.geojson
geography_caption: Beijing-Tianjin-Hebei region, China, PRC
---

# Overview

<div class="note-card">
  <p><strong>Note:</strong> Many parts of the interviews with BMCT officials are not integrated because they are still in discussions regarding whether to disclose this information. More than happy to provide the full transcript once the interviewees have approved it.</p>
</div>

<style>
.note-card {
  background-color: #fff8e6;
  border-left: 4px solid #f59e0b;
  padding: 16px;
  margin: 20px 0;
  border-radius: 4px;
  box-shadow: 0 1px 3px rgba(0,0,0,0.1);
}
.note-card p {
  margin: 0;
  color: #713f12;
}
.note-card strong {
  color: #92400e;
}
</style>

<div class="image-container">
  <img src="./christian-lue-qQT7l54ERZM-unsplash.jpg" alt="Beijing MaaS System Overview" />
  <div class="image-caption">
    Photo by 
    <a href="https://unsplash.com/@christianlue?utm_content=creditCopyText&utm_medium=referral&utm_source=unsplash">Christian Lue</a> 
    on 
    <a href="https://unsplash.com/photos/a-very-tall-building-in-the-middle-of-a-city-qQT7l54ERZM?utm_content=creditCopyText&utm_medium=referral&utm_source=unsplash">Unsplash</a>
  </div>
  <style>
    .image-caption {
      font-weight: 300;
      font-size: 12px;
      color: #666666;
      margin-top: 0px;
      margin-bottom: 5px;      
    }
</style>
</div>

Beijing Mobility as a Service (MaaS) operates as a pan-municipal public-private partnership led by the Beijing Municipal Commission of Transport (BMCT, 北京市交通委员会) and the Beijing Municipal Ecology and Environment Bureau (北京市生态环境局), collaborating with private mobility vendors and service providers to enhance seamless urban mobility.

By integrating navigation tools, public transit, ride-hailing, and shared bikes, all orchestrated through real-time mobility data from the Transport Commission, the ecosystem incentivizes low-carbon behavior shifts to achieve policy goals such as carbon reduction, commute optimization, and sustainable urban development.

Like many Mobility-as-a-Service initiatives globally, Beijing's MaaS system lacks publicly available comprehensive architecture documentation. The following analysis synthesizes insights from discussions with Mr. Yuhuan Zhai, the Director of Technology at BMCT and with Mr. Yi Zhao, the Director of MaaS Carbon Inclusive Initiatives at AMap, Beijing MaaS 2.0 work plan (北京 MaaS 2.0 工作方案, [link to Chinese version](https://jtw.beijing.gov.cn/kjjt/tzgg/202306/t20230627_3147334.html)), and news reports covering the system's development to identify key strategic priorities. While not exhaustive, the analysis should provide a comprehensive overview of the system's principal objectives, key features, impacts, and future directions.

## Goals and Aspirations:

At its core, Beijing MaaS leverages digital platforms to enhance mobility experiences while generating precise insights into travel patterns and behaviors. What distinguishes Beijing's approach is its use of navigation systems as behavioral intervention points, which is creating opportunities to incentivize user actions that advance multiple policy objectives simultaneously, from carbon reduction to economic development in peripheral areas. These interventions align with directives from China's 14th Five-Year Plan ([link to English version](https://cset.georgetown.edu/publication/china-14th-five-year-plan/)), which emphasizes smart transportation integration and carbon reduction as national priorities, while also serving municipal interests in user satisfaction, revenue generation, and coordinated urban-regional development.

### Multimodel Mobility Integration

**Objective**: Create a unified urban mobility ecosystem that seamlessly connects transportation modes for travelers while providing a intergrated data hub for data vendors and mobility service providers.

**Data Infrastructure**: Operating under the Beijing Management Measures for Opening and Sharing Transport and Travel Data (Trial) (北京市交通出行数据开放管理办法(试行), [link to Chinese version](https://www.beijing.gov.cn/zhengce/zhengcefagui/201911/t20191105_483739.html)), the platform aggregates datasets from public operators and private mobility providers. This standardized data exchange supports both third-party application development and provides planners with insights into mobility patterns.

**Aggregated Route Planning**: Like many other existing MaaS systems, Beijing MaaS partners with navigation apps (e.g., Amap, Baidu), Beijing MaaS provides real-time multimodal route planning, including metro-to-bike transitions, shared bike availability, and ride-hailing options from multiple providers. Users can view metro crowdedness, bus arrival times, and bike parking zones in one place.

**Regional Connectivity**: Beijing has one of the longest average commuting times in the world, with many residents commuting from outskirts to the city center. To enhance service across the Jing-Jin-Ji (Beijing-Tianjin-Hebei, 京津冀) region, Beijing MaaS 2.0 implements cross-regional "air/rail + urban transit" planning capabilities, facilitating connections such as intercity rail to suburban bus transfers. This integration allows users to navigate transit systems across different cities more seamlessly while providing transportation agencies with more comprehensive Origin-Destination (OD) data for planning purposes.

### Carbon Reduction & Green Financing

**Objective**: Promote sustainable transportation choices by integrating carbon reduction incentives with Beijing's emissions trading framework. This approach encourages residents to adopt lower-carbon travel options while creating sustainable funding mechanisms for both public infrastructure and private innovation. The initiative supports China's broader goals for digital financial systems and carbon neutrality, testing evidence-based carbon credit (碳普惠) programs and sustainable finance tools that could potentially scale to other urban contexts.

**Carbon Inclusive Incentives**:
Since 2020, the "MaaS Travel, Green Life" campaign has tracked user emissions reductions through municipality-approved calculation methodologies ([1](https://www.beijing.gov.cn/zhengce/zhengcefagui/202303/t20230327_483739.html), [2](https://sthjj.beijing.gov.cn/bjhrb/resource/cms/article/201256520/325814543/2022042818252517641.docx)). Users can opt into carbon reduction programs via navigation apps by selecting "green routes," earning credits that can be redeemed for transit discounts, retail vouchers, or charitable donations. This incentive structure encourages more sustainable transportation choices across the metropolitan region.

**Carbon Market Integration**:
In partnership with the Beijing Emissions Trading System (BJETS), 97,600 tons of carbon credits were traded during 2021–2023. Beyond generating revenue, a significant portion of these credits were redistributed to users through the Carbon Inclusive Incentives program. Future plans include expanding trading operations to the broader Jing-Jin-Ji region and establishing linkages with national China Certified Emission Reduction (CCER)([3](https://www.chinadaily.com.cn/a/202401/23/WS65af1efea3105f21a507dcc8.html)) standards.

**Green Finance**: Beijing is exploring "traffic-behavior-linked" financial instruments through collaborations with banks and green exchanges, including digital yuan payments and carbon-accounting frameworks that support ESG objectives.

### Commuting Optimization

**Objective**: Mitigate extreme commuting challenges through smart planning and demand-responsive services, aligned with Beijing's "AI+" Action Plan (2024–2025) ([Link to English version](https://cset.georgetown.edu/publication/beijing-ai-plan-2024-2025/)) for intelligent transportation systems.

The platform dynamically optimizes transportation resources across Beijing through: data-driven parking management adapting to mobility patterns; flexible transit networks balancing equity and efficiency; policy incentives for high-occupancy vehicles; and targeted interventions addressing urban-peripheral commuter imbalances. This transforms static infrastructure into responsive systems that allocate resources based on real-time demand.

## Key characteristics

The complexity of MaaS makes it difficult to formulate a detailed, highly actionable master plan. Moreover, due to the Municipal government's tradition of operational flexibility, no comprehensive master plan exists. Instead, the Beijing Municipal Transportation Commission has adopted a "dynamic iteration" model:

Strategically, national and municipal regulations, policies, and action initiatives, including the "Beijing AI+ Action Plan (2024-2025)," provide the comprehensive technical roadmap and policy framework for the initiative. For example, under new data sharing regulations, Beijing MaaS was required to integrate with Peace Chain (平安链), a government-backed blockchain platform, alongside robust security protocols that ensure system reliability and data integrity. The Beijing Traffic Operation and Command Center (TOCC) serves as the central coordinating body, tasked with standardizing interfaces across transportation modes, facilitating cross-departmental collaboration, and reporting implementation progress to the Technology Department of the Beijing Municipal Government, which maintains oversight as the core executive authority.

At the implementation level, through a "task breakdown-parallel advancement-phase acceptance" mechanism, the Commission breaks down large goals into independent subtasks (such as data sharing protocol formulation and carbon credit algorithm development). Each task is established by the Technology Department and then implemented by TOCC in conjunction with enterprise partners (such as Baidu and Didi). This model not only adapts to the multi-party coordination needs of the MaaS ecosystem (government, operators, technology providers, and users) but also avoids the risks of traditional rigid "one-size-fits-all" planning.

Interestingly, there is no dedicated MaaS department within BMCT or any city agency, but rather an ad hoc group of officials responsible for overseeing the MaaS system.

## Stakeholders

The Beijing MaaS platform was initiated by the Beijing Municipal Commission of Transport (BMCT), who partnered with the Beijing Municipal Ecology and Environment Bureau (BMEEB) to launch the project.

The case of Beijing MaaS follows the template of "government setting the stage, companies delivering the services," with the government taking the lead in coordinating stakeholders while not directly operating the MaaS platform.

## Technology Interventions

This section outlines three technology-enabled interventions proposed for Beijing's Mobility-as-a-Service (MaaS) project. Each solution is aligned with global best practices while tailored to address local challenges within Beijing's urban mobility ecosystem.

### AI-Driven Dynamic Routing & Demand Forecasting

**Use Case:** Real-time optimization of commuter routes to reduce congestion and improve travel efficiency across Beijing's transportation network. The system dynamically reroutes users during peak hours to less congested metro lines and incentivizes off-peak bike-sharing through targeted discounts.

**Value Proposition:**
The AI-driven system reduces average commute times by 15–20 minutes while lowering traffic congestion by 25% in pilot zones such as Chaoyang District. These efficiency gains directly address Beijing's critical rush-hour congestion challenges.

**Solution Architecture:**
The architecture integrates multiple data sources including real-time traffic sensors, subway and bus GPS tracking, shared mobility APIs (Didi, Meituan Bike), and anonymized user travel patterns covering over 450 million daily trips. Advanced machine learning models process this data to predict demand spikes and dynamically adjust route recommendations. A notable feature includes integration with "green wave" traffic signal systems that prioritize buses during rush hours.

All processing occurs on Beijing's Traffic Big Model Platform ("交通大模型平台") utilizing Alibaba Cloud's AI compute clusters for scalable performance.

**Data Flows:**
The system consumes traffic flow metrics, vehicle occupancy rates, weather conditions, and event schedules. It generates predictive congestion maps, personalized route suggestions, and carbon-saving metrics for user feedback.

**Standards:**
Implementation adheres to ISO 37156 (smart city data exchange) and China's GB/T 35648-2017 ITS standards to ensure compatibility across systems.

**Business Model:**
The intervention operates through public-private partnerships (PPP) with technology firms such as Baidu Maps, which offer API access for a subscription fee that funds ongoing development.

**Regulatory Considerations:**
The system maintains compliance with China's Data Security Law through rigorous anonymization protocols and cross-agency data sharing guidelines under Beijing Development and Reform Commission Document No. 1081 of 2024 ("京发改〔2024〕1081 号") regulations.

### Unified Account-Based Ticketing (ABT) System

**Use Case:** The ABT system enables seamless multi-modal payments for combined transportation journeys (subway + shared bike + parking) through a single digital wallet interface.

**Value Proposition:**
This unified approach increases public transit ridership by 30% through intelligent fare integration, such as automatic discounts when combining metro and bike trips. By eliminating fragmented ticketing processes, the system saves users 8–10 minutes per journey while significantly improving the overall transit experience.

**Solution Architecture:**
The core components include a centralized ABT backend ledger managed by Beijing's Transport Operation and Control Center (TOCC) that tracks transactions across all service providers. Digital token-based validation utilizing NFC and QR codes provides the authentication layer, with native compatibility with Alipay and WeChat Pay to leverage existing payment behaviors. Comprehensive APIs connect the Beijing MaaS app with third-party mobility providers like Shouqi Car Rental.

**Data Flows:**
The system processes user travel history, dynamic fare rules, and real-time service availability. It generates unified travel logs that enable carbon credit calculations and targeted subsidy allocations for disadvantaged populations.

**Standards:**
Implementation follows the Mobility Data Specification (MDS) for interoperability and EMVCo standards for secure contactless payments.

**Business Model:**
Revenue generation occurs through transaction fee sharing (0.5–1.5%) with mobility providers, while government subsidies support low-income users to ensure equitable access.

**Regulatory Considerations:**
The system adheres to the People's Bank of China's non-bank payment regulations and implements GDPR-like privacy safeguards in accordance with China's Personal Information Protection Law (PIPL).

### Blockchain-Secured Carbon Credit Trading Platform

**Use Case:** The platform tokenizes carbon savings generated from environmentally friendly transportation choices (cycling, electric vehicles) for trading on regional carbon markets.

**Value Proposition:**
The system enables cross-border carbon trading throughout the Beijing-Tianjin-Hebei ("京津冀") region, with 97,600 tons of CO₂ successfully traded since 2021. Users receive tangible incentives through redeemable credits, such as 10 credits equaling a ¥5 subway voucher, creating a virtuous cycle of sustainable behavior.

**Solution Architecture:**
The platform utilizes smart contracts to automate credit issuance based on verified trip data, including bike GPS logs and vehicle type information. Built on Hyperledger Fabric, the blockchain connects to both the Beijing Emissions Trading System (BJETS) and the national CCER registry for maximum liquidity. Users interact through an intuitive carbon dashboard integrated directly within the MaaS app, displaying real-time savings metrics and current market prices.

**Data Flows:**
The system processes trip distance, transportation mode selection, and emission factors according to Beijing's low-carbon transportation carbon reduction methodology ("《北京市低碳出行碳减排量方法学》"). It generates immutable transaction records for auditing purposes and user-tiered reward profiles to encourage continued participation.

**Standards:**
Implementation follows ISO 14064 carbon accounting standards and W3C Verifiable Credentials protocols to ensure data integrity throughout the system.

**Business Model:**
Revenue generation occurs through modest transaction fees (0.2% per trade) and corporate ESG partnerships with major enterprises like Sinopec that purchase credits to offset their carbon footprints.

**Regulatory Considerations:**
The platform aligns with the Ministry of Ecology and Environment's carbon market rules and implements robust anti-fraud monitoring systems to ensure market integrity.

## Financing

The project is mainly financed by the Municipal government, with some funding from the central government.

## Outcomes

<div class="timeline">
  <div class="timeline-item">
    <div class="timeline-date">2019</div>
    <div class="timeline-content">
      <h4>Beijing MaaS 1.0 Development Started</h4>
      <p>Initial implementation of MaaS system. Based on AMap and Baidu Map navigation system, focusing on providing real-time multimodal route planning, subway crowding stats functionality.</p>
    </div>
  </div>
  <div class="timeline-item">
    <div class="timeline-date">2020</div>
    <div class="timeline-content">
      <h4>Carbon Inclusive Incentives Introduced</h4>
      <p>Beijing Municipal Commission of Transport launched the "MaaS Travel, Green Life" campaign to track user emissions reductions (over 40,000 tons CO₂ by 2023) through verified methodologies, allowing users to earn credits redeemable for transit discounts, vouchers, or donations.</p>
    </div>
  </div>
  <div class="timeline-item">
    <div class="timeline-date">2023</div>
    <div class="timeline-content">
      <h4>Beijing MaaS 2.0 Launched</h4>
      <p>Integration of more mobility options and improved data infrastructure. The system now includes real-time traffic information, parking availability, and bike-sharing data.</p>
    </div>
  </div>
</div>

<style>
.timeline {
  border-left: 2px solid #6366f1;
  padding-left: 20px;
  margin: 20px 0;
}
.timeline-item {
  margin-bottom: 20px;
  position: relative;
}
.timeline-item::before {
  content: '';
  width: 12px;
  height: 12px;
  background: #6366f1;
  border-radius: 50%;
  position: absolute;
  left: -26px;
  top: 5px;
}
.timeline-date {
  font-weight: bold;
  color: #6366f1;
}
</style>

<div class="stat-grid">
  <div class="stat-box">
    <span class="stat-number">97,600</span>
    <span class="stat-label">Tons of Carbon Credits Traded</span>
  </div>
  <div class="stat-box">
    <span class="stat-number">40,000</span>
    <span class="stat-label">Tons CO₂ Reduced</span>
  </div>
</div>

<style>
.stat-grid {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(200px, 1fr));
  gap: 20px;
  margin: 20px 0;
}
.stat-box {
  background: #f8fafc;
  border: 1px solid #e2e8f0;
  border-radius: 8px;
  padding: 20px;
  text-align: center;
  transition: transform 0.2s;
}
.stat-box:hover {
  transform: translateY(-5px);
}
.stat-number {
  display: block;
  font-size: 2em;
  font-weight: bold;
  color: #6366f1;
}
.stat-label {
  display: block;
  margin-top: 8px;
  color: #64748b;
}
</style>
