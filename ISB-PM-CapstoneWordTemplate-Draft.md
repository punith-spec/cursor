# ISB PM Capstone Report Draft  
**Role:** VP of Product, Rakuten India  
**Product:** Rakuten Smart Catalog Assistant (SCA)  

---

## 1. Project Overview and Objectives

As VP of Product at Rakuten India, I am leading the launch of **Rakuten Smart Catalog Assistant (SCA)**, a B2B AI-powered catalog and merchant tooling suite that helps marketplace sellers create cleaner, richer, and higher-performing listings across Rakuten’s e-commerce ecosystem.  

SCA addresses a common merchant challenge: creating and maintaining high-quality product data at scale. Poor listing quality leads to lower discoverability, lower conversion, compliance errors, and inefficient operations. By automating core listing tasks (title generation, attribute completion, image checks, policy guardrails), SCA improves seller productivity while directly supporting Rakuten’s business outcomes: better shopper experience, stronger retention, and increased GMV.

### Year 1 Business Objectives
- Increase **catalog data completeness** (mandatory attributes filled) from **78% to 95%** for active merchants.
- Improve **search/recommendation CTR** on product detail and listing surfaces by **10%**.
- Reduce **merchant listing time per SKU** by **40%** through automation.
- Deliver **3-5% GMV uplift** attributable to catalog quality and conversion improvements.

---

## 2. Product Concept, Market Opportunity, and Target Segments

### 2.1 Product Concept

**Rakuten Smart Catalog Assistant** is a cloud-native product embedded into the Rakuten Merchant Console. It uses AI to improve listing quality before products go live.

Core capabilities:
- **AI content optimization:** Generates and improves product titles, bullets, and descriptions using category context, brand tone, and shopper search behavior.
- **Attribute automation:** Auto-fills and validates key attributes (size, material, compatibility, etc.) from images, PDFs, and feed inputs.
- **Compliance guardrails:** Flags restricted claims, missing disclosures, format issues, and policy violations pre-publication.
- **Listing quality score:** Provides actionable recommendations (e.g., image quality upgrades, missing technical specs, clarity improvements).
- **Tiered experience:** Free baseline for all merchants; advanced bulk/API/governance features for Pro and Enterprise tiers.

### 2.2 Market Opportunity

Marketplace growth depends heavily on product data quality. Better listings improve ranking, recommendation relevance, buyer trust, and conversion.

Current merchant pain points:
- Fragmented and inconsistent source data across tools and teams.
- Limited content and SEO expertise for ongoing optimization.
- High operational effort for manual listing and corrections.
- Rework and delays caused by compliance and quality errors.

Strategic opportunity for Rakuten:
- **Retention:** Make Rakuten easier to sell on through productivity tooling.
- **Differentiation:** Compete on seller experience and intelligence, not only fees.
- **Monetization:** Introduce recurring revenue through premium merchant tooling.

### 2.3 Target Customer Segments

1. **Tier-1 Strategic Merchants (10k+ SKUs)**  
   - Pain: bulk catalog complexity, quality inconsistency across regions, high ops cost.  
   - Value from SCA: APIs, governance controls, large-scale optimization, SLA-backed workflows.

2. **Mid-Market Digital-First Brands (500-10k SKUs)**  
   - Pain: limited team bandwidth and frequent listing updates.  
   - Value from SCA: guided authoring, smart templates, fast edits, measurable quality gains.

3. **Long-Tail Small Sellers (<=500 SKUs)**  
   - Pain: low tooling maturity and listing friction.  
   - Value from SCA: wizard-style UX, one-click suggestions, built-in guardrails.

---

## 3. Strategic Development Plan

### 3.1 Discovery and Validation Plan

**Discovery approach**
- Conduct 20-30 in-depth merchant interviews across all three segments.
- Map current listing workflows, SLA bottlenecks, and common quality defects.
- Analyze baseline metrics: missing attributes, rejection reasons, edit loops, approval times.
- Benchmark internal and competitor merchant tooling standards.

**Validation approach**
- Build category-specific hypotheses (starting with Electronics and Fashion).
- Quantify value via A/B testing against control groups.
- Define launch thresholds for accuracy, acceptance rate, and compliance safety.

### 3.2 Phased Rollout Roadmap

1. **Alpha (Internal, 3 months)**  
   - Use historical catalog and moderation data to train and test models.  
   - Internal users: catalog ops and policy teams.  
   - Success checks: suggestion precision, manual edit reduction, policy false-positive rate.

2. **Beta (Merchant Pilot, 3 months)**  
   - Pilot with 50 merchants across Tier-1 and mid-market segments in 2 categories.  
   - Run structured A/B tests against control cohorts.  
   - Measure: time-to-list, attribute completeness, approval turnaround, CTR/conversion impact.

3. **Scaled Rollout (6-9 months)**  
   - Expand category and region coverage.  
   - Launch premium plans and refine onboarding/GTM based on pilot outcomes.  
   - Establish continuous model retraining and product instrumentation loops.

### 3.3 Positioning Strategy

**Positioning statement**  
*“Rakuten Smart Catalog Assistant is your AI partner for clean, complete, and conversion-ready product listings, so your team spends less time fixing catalogs and more time growing sales.”*

Positioning pillars:
- **Accuracy and Compliance:** trustworthy, policy-aware listing support.
- **Productivity and Speed:** faster listing creation with fewer revisions.
- **Growth Impact:** higher discoverability and conversion through better catalog quality.

Differentiators:
- Native integration with Rakuten’s ranking, recommendation, and policy systems.
- Category-aware guidance tuned for how Rakuten approves and ranks products.
- Leverages Rakuten India’s cross-domain strengths across commerce, fintech, mobile, and AI.

### 3.4 Pricing Strategy

**Value-based tiering**
- **Basic (Free):** single-SKU assist, baseline quality score, limited suggestions.  
  - Goal: broad adoption and baseline catalog improvement.
- **Pro (e.g., $99/month/account):** bulk optimization, feed ingestion, richer suggestions, workflow integrations.  
  - Target: mid-market brands and scaling merchants.
- **Enterprise (custom pricing):** API access, advanced controls, multi-region governance, dedicated support, SLAs.  
  - Target: strategic enterprise accounts.

Price validation:
- Run willingness-to-pay experiments during beta.
- Compare perceived value against quantified time savings and defect reduction.
- Package features by operational and revenue impact rather than pure usage volume.

### 3.5 Go-to-Market (GTM) Strategy

**Primary channels**
- In-product discovery in Merchant Console.
- Merchant success and account management for high-value segments.
- Webinars, enablement content, and case studies.

**GTM sequence**
1. Internal enablement (playbooks, demos, objection handling, ROI narratives).  
2. Publish pilot success stories (time savings + conversion lift).  
3. Launch campaign with adoption incentives (e.g., 3-month Pro trial).  
4. Ongoing in-product nudges and guided actions using quality score insights.

---

## 4. Performance Metrics and AI Integration

### 4.1 AI Integration Approach

SCA combines multiple AI components:
- **NLP/GenAI:** improves listing text while enforcing marketplace policies.
- **Computer vision:** infers attributes from product images and highlights image quality gaps.
- **Ranking-aware recommendation logic:** prioritizes suggestions with strongest correlation to CTR and conversion uplift.
- **Human-in-the-loop controls:** allows merchants and ops teams to review/override sensitive outputs.

### 4.2 KPI Framework

**1) Business Impact**
- GMV uplift for SCA users vs matched controls.
- Incremental subscription revenue from Pro/Enterprise tiers.
- Merchant retention and account expansion metrics.

**2) Operational Efficiency**
- Time-to-list per SKU (before vs after SCA).
- Manual edit rate of AI-generated outputs.
- Catalog approval turnaround and rejection rate.

**3) Model/Product Performance**
- Suggestion acceptance rate.
- Attribute extraction accuracy vs human-reviewed benchmark.
- Policy violation and hallucination rate (must trend downward).

**4) Merchant Experience**
- SCA CSAT/NPS.
- Engagement depth (suggestions applied/session, repeat use, feature breadth).
- Support volume linked to listing quality issues.

---

## 5. Long-Term Recommendations

1. **Expand category and regional depth**  
   - Move beyond initial categories into Home, Grocery, and specialty verticals with localized policy and language support.

2. **Increase personalization**  
   - Adapt recommendations to merchant maturity, brand voice, catalog history, and performance patterns.

3. **Build ecosystem-level orchestration**  
   - Integrate listing intelligence with ads, pricing, and promotions to deliver unified optimization guidance.

4. **Institutionalize AI governance**  
   - Formalize model monitoring, fairness checks, and human review workflows for sensitive categories and claims.

5. **Strengthen feedback loops**  
   - Capture explicit merchant feedback on recommendations and use it for continuous model and UX calibration.

---

## Conclusion

Rakuten Smart Catalog Assistant is a strategically aligned product that improves merchant productivity and catalog quality while driving measurable commercial outcomes for Rakuten. By combining AI automation with strong governance, clear pricing, and phased GTM execution, SCA can become a durable merchant platform advantage that improves discovery, conversion, and seller loyalty across the Rakuten ecosystem.
