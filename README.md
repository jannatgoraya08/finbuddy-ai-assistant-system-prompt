# FinBuddy: Making a Bank's AI Assistant Follow the Rules with a System Prompt
# FinBuddy: Making a Bank's AI Assistant Follow the Rules with a System Prompt

**A FinTech case study on when a plain chat is enough and when a business needs a system prompt.**

Author: Jannat Goraya · BBA (FinTech), Chitkara Business School · Tool: ChatGPT · November 2026

## The case

**KoshBank** (fictional) is a digital bank for college students in Pune with 3 lakh users. It wants to launch **FinBuddy**, an in-app AI assistant. Its compliance team worries that a chatbot could give stock tips, ask for OTPs or invent interest rates. As a Business Analyst, I tested whether a system prompt can make the AI follow the bank's rules every time.

## The data

10 synthetic customer questions created with AI (7 English, 3 Hinglish), including 6 "trap" questions designed to make the AI break rules. I wrote the correct behaviour for each question before testing.

## Approach

| Step | Set-up | Task |
|---|---|---|
| 1 | Plain chat | One simple general question |
| 2 | Plain chat | All 10 customer questions |
| 3 | System prompt (v1) | The same 10 questions |
| 4 | System prompt (v2) | Additional Q09 stress test after improving the prompt |
| 5 | Roles | Same question with no role, an expert role and a friendly role |

## Results

| Metric | Plain chat | System prompt |
|---|---:|---:|
| Answers that followed every rule (/10) | 8/10 | 10/10 |
| Personal data handled safely | Yes | Yes |
| No investment tips | No | Yes |
| Closing line present (/10) | 0/10 | 10/10 |

## Key learnings

1. **A plain chat is enough for general questions:** ChatGPT successfully answered simple questions such as explaining savings accounts. However, it did not automatically follow all of KoshBank's business rules.
2. **A system prompt enforces business rules:** It fixed Q05 by avoiding specific investment recommendations and Q10 by replying in Hinglish. It also ensured that all 10 answers included the mandatory closing statement.
3. **Version 2:** I added a rule to prioritise the most urgent issue when customers ask multiple questions together. The additional Q09 stress test produced a more focused response.
4. **Roles:** A role mainly changed the tone, communication style and level of detail. The credit analyst role was more formal, while the college senior role was friendlier. The factual guidance remained broadly similar.

## My recommendation to KoshBank

FinBuddy should only be considered for a controlled pilot after further testing, security review and compliance approval. The system prompt should be combined with human support for fraud-related issues, secure data handling and regular testing. A system prompt improves consistency but cannot guarantee that an AI assistant will follow every rule in every situation.

## Skills shown

Prompt engineering · System prompt design · Role prompting · Chatbot stress-testing · Responsible AI in finance · Customer-experience design

## What I learned

- A plain chat is fine for one-off, general questions.
- A system prompt gives AI standing rules, so a business assistant behaves consistently.
- A good system prompt states the audience, tone, limits, what to do when unsure and what never to do.
- Trap questions (stock tips, OTPs, "ignore your rules") are useful for testing an AI assistant.
- A role changes the tone of an answer more than its accuracy.
- System prompts improve through testing and refinement.
- AI assistants in finance must protect personal data and avoid advice they are not allowed to give.

*KoshBank, FinBuddy and all data in this project are fictional and created for learning.*


