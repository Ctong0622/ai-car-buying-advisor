# AI Car Buying Advisor — Final Project Proposal

## Three Ideas

**Idea 1: AI Car Buying Advisor**

A website that helps people choose a new or used car based on their budget, preferences, and driving needs. AI will recommend suitable vehicles and explain the advantages and disadvantages of each option.

**Idea 2: AI Travel Planner**

A website that helps students plan trips based on their budget, destination, and interests. AI will suggest activities and create a simple travel itinerary.

**Idea 3: AI Study Planner**

A website that helps college students organize assignments and exams. AI will recommend a study schedule based on deadlines and available time.

## Why I Chose This Idea

I chose AI Car Buying Advisor because I am interested in cars and often compare different models, prices, and features. I also have friends who ask for advice when choosing a car.

I did not choose the travel planner because there are already many similar tools, and I am less interested in building one.

I did not choose the study planner because I have already worked on student productivity tools in previous mini projects. I want to try something different for my final project.

## What I Am Building

I am building an AI-powered car recommendation website that helps users compare new and used vehicles.

Users will enter their budget, preferred vehicle type, new or used condition, and priorities. The website will send this information to an AI model with specific instructions and return personalized car recommendations.

The goal is to help users narrow down their choices and understand why certain cars might fit their needs.

## Who It Is For

The main user will be a friend or classmate who is considering buying a car but does not know which model to choose.

This person may have a specific budget but may not understand the differences between vehicle models, reliability, maintenance costs, and features.

I want to create a simple website that helps this person make a more informed decision without spending hours researching different cars.

I will ask a friend or classmate to test the website after it is built and use their feedback to improve it.

## What the User Does

1. Open the website.
2. Enter a budget in USD.
3. Select new, used, or either.
4. Select a preferred vehicle type, such as sedan, SUV, coupe, or no preference.
5. Choose priorities such as reliability, performance, comfort, fuel economy, or luxury.
6. Click the recommendation button.
7. Read up to three AI-generated vehicle recommendations.
8. Compare the recommendations and their advantages and disadvantages.

## Data

The website will collect the following information from the user:

- Budget in USD
- New or used preference
- Vehicle type
- Main priorities
- Optional additional preferences

The application will send these inputs to an AI model through a server-side function.

The AI model will generate recommendations based on its general knowledge and the user's preferences.

The first version will not use a live dealership inventory or pricing database. The website will clearly explain that prices are estimates and that users should verify current prices, availability, vehicle history, and condition before making a purchase.

I do not plan to store personal information or user accounts in the first version.

## AI Feature

The main feature is an AI-powered car recommendation system.

Unlike a general chatbot, the AI will receive specific instructions written for this application.

The AI will be instructed to:

- Recommend up to three vehicles that fit the user's budget and preferences.
- Consider both new and used cars depending on the user's selection.
- Explain why each vehicle is suitable.
- Mention important advantages and disadvantages.
- Consider reliability, maintenance costs, comfort, performance, and other selected priorities.
- Avoid inventing exact dealership prices or claiming that a specific vehicle is currently available.
- Explain uncertainty when information may be outdated.
- Present recommendations in simple language that is easy to compare.

For example, a user might enter a $30,000 budget, select a used SUV, and prioritize reliability and comfort.

The AI should recommend realistic vehicles, explain why they fit, and identify possible disadvantages.

The website will not simply send a user's message to a general chatbot. It will use a structured form and its own instructions to generate recommendations for a specific car-buying decision.

## Main Features

1. **Car Preference Form:** Users enter their budget, condition preference, vehicle type, and priorities.
2. **AI Recommendations:** The website generates up to three personalized vehicle suggestions.
3. **Car Comparison:** Each recommendation includes an explanation, advantages, and disadvantages.
4. **Helpful Warnings:** The website reminds users to verify prices, maintenance history, and vehicle condition.
5. **Responsive Design:** The website should be readable and usable on a laptop or phone.

## States and Tests

I will design and test the following states before considering the application complete.

### 1. Empty State

**State:** The user has not entered any information.

**Test:** Open the website without filling in the form.

**Expected Result:** The form is visible with clear instructions, and no recommendations are displayed.

### 2. Loading State

**State:** The user has submitted valid preferences and the AI request is processing.

**Test:** Enter valid preferences and click the recommendation button.

**Expected Result:** The website displays a loading message and prevents accidental repeated submissions while waiting.

### 3. Success State

**State:** The AI successfully returns recommendations.

**Test:** Enter a $30,000 budget, select a used SUV, and choose reliability and comfort.

**Expected Result:** The website displays up to three relevant recommendations, with explanations, advantages, and disadvantages.

### 4. Invalid Budget

**State:** The user enters an invalid budget.

**Test:** Enter a negative number, zero, or nonnumeric text.

**Expected Result:** The website displays a clear validation message and does not send the request.

### 5. Missing Preferences

**State:** The user does not complete a required field.

**Test:** Leave the budget empty and try to submit.

**Expected Result:** The website asks the user to enter a valid budget.

### 6. API Error

**State:** The AI service is unavailable or the request fails.

**Test:** Temporarily use an invalid API configuration in the development environment.

**Expected Result:** The website displays a friendly error message and allows the user to try again.

### 7. Long AI Response

**State:** The AI returns more text than expected.

**Test:** Request recommendations with several priorities and inspect a longer response.

**Expected Result:** The text remains readable, and the layout does not break.

### 8. Missing API Configuration

**State:** The server does not have a valid AI API key.

**Test:** Run the server-side function without the required environment variable in a development environment.

**Expected Result:** The website shows an understandable error without revealing private configuration information.

## AI Technical Experiment

Before building the full application, I need to verify that I can successfully call an AI model from a server-side function.

I plan to create a small test that sends a sample car-buying request to the model with my own instructions.

**Sample Input:**

- Budget: $30,000
- Condition: Used
- Vehicle Type: SUV
- Priorities: Reliability and comfort

**Expected Output:**

The model should return up to three realistic vehicle suggestions, explain why they fit, and mention possible disadvantages. It should avoid claiming that prices or dealership availability have been verified.

**What I Need to Check:**

- Whether the API request succeeds.
- Whether the server can receive and process the response.
- Whether the recommendations follow my instructions.
- Whether the API key stays hidden from the browser.
- Whether errors are handled correctly.

**Experiment Status:** Not tested yet. I will record the actual request, result, and any problems after running the experiment.

## What I Do Not Know Yet

I have not built a website that calls an AI model through a server-side function before.

I need to learn how to connect the frontend to the AI service, protect the API key, and handle unsuccessful requests.

I also need to figure out how to make the AI recommendations consistent and useful for different budgets and preferences.

Another challenge is accuracy. Car prices change, especially for used vehicles. I need to make sure the website does not present AI estimates as verified current market prices.

My goal is to build a simple and useful car recommendation website rather than a complicated car marketplace.
