# Slice — Smart Spending Assistant

## Overview

This project proposes a **Smart Spending Assistant for Slice** that helps users move from simply looking at past transactions to understanding and planning their future spending.

> **Don't just tell users where their money went. Help them understand where their spending is heading.**

The solution uses transaction history to build a personalised spending baseline, identify unusual behaviour, add financial context, and provide a recommended spending limit for the coming week.

## The Problem

Traditional spending views are mostly reactive. Users can see their past transactions, but still have to figure out:

- Am I spending more than usual?
- Am I likely to overspend next week?
- How much can I safely spend?
- Which category is causing my spending to increase?

The problem is therefore not a lack of data — it is a lack of **actionable context**.

## Proposed Solution

The proposed feature introduces a **Spending Behaviour Engine** with three main lenses:

### 1. Weekly Lens
Compares current weekly spending with the user's historical weekly average to identify unusual spending.

### 2. Category Lens
Looks at spending category-wise to understand what is driving the change.

### 3. Financial Lens
Combines spending behaviour with budget and savings context to understand what the change means for the user's financial position.

These signals are then passed to an ML layer to predict upcoming spending and generate a personalised recommended spending limit.

## How It Works

```text
Transaction History
        ↓
Weekly & Category Aggregation
        ↓
Behavioural Baseline & Deviations
        ↓
Financial Context Analysis
        ↓
ML Prediction
        ↓
Recommended Spending Limit
        ↓
Actionable Insights
```

## New User Experience

The proposed UI adds a prominent **Spending Insights** card to the home screen.

It can show:

- Recommended spending limit
- Predicted spending
- Change compared with last week
- Progress towards the recommended limit
- Four-week spending average
- Quick spending trend
- A short explanation of the recommendation

Users can open a detailed **Spending Insights** screen to view prediction vs. historical spending, the four-week average, recent transactions, and supporting insights.

## Product Flow

1. Collect transaction history.
2. Aggregate spending by week and category.
3. Build a personalised historical baseline.
4. Detect deviations from normal behaviour.
5. Add financial context such as budget and remaining savings.
6. Predict upcoming spending.
7. Generate a recommended spending limit.
8. Show the recommendation clearly to the user.
9. Track outcomes and use feedback to improve future predictions.

## Product Goal

The goal is **not to restrict spending**.

It is to give users useful context early enough to make better decisions, stay in control of their spending, and make progress towards their savings goals.

## Key Metrics

Potential success metrics include:

- Prediction accuracy
- Recommendation adherence
- Reduction in unexpected overspending
- Engagement with Spending Insights
- Change in weekly spending behaviour
- Progress towards savings goals

## Project Status

This repository contains the product concept, proposed architecture, feature flow, and UI direction for the Smart Spending Assistant.

The implementation can be extended with a real transaction dataset and an ML model for spending prediction and recommendation generation.
