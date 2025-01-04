# 📧 Cold Email Generator for Services Companies

## Overview
This project is a **Cold Email Generator** built using **Groq**, **LangChain**, and **Streamlit**. It enables services companies to generate highly personalized cold emails to pitch their services to other businesses. The tool is specifically designed to streamline the process of identifying job openings on a company's careers page and crafting tailored outreach emails.

### Core Features:
1. **URL Input for Careers Page**: Users can input the URL of a company's careers page.
2. **Job Listings Extraction**: The tool extracts job postings from the provided URL.
3. **Vector Database Integration**:
   - Portfolio links (documents, projects, or case studies) are stored in a vector database.
   - Links are matched to the extracted job descriptions using semantic similarity.
4. **Cold Email Generation**:
   - Personalized emails are generated based on the job descriptions and matched portfolio links.

---

## Use Case Scenario
### Business Context:
Nike is searching for a **Principal Software Engineer** and investing significant time and resources in the hiring process, onboarding, and training. Atliq, a software development company, can offer a **dedicated software development engineer** as a solution to Nike's immediate needs.

### Cold Email Objective:
Mohan, a Business Development Executive from Atliq, plans to reach out to Nike via a cold email. The email will:
- Highlight Atliq's capability to address Nike's software development needs.
- Showcase relevant experience and portfolio links.
- Demonstrate the value of Atliq’s services in reducing Nike's hiring effort.

---

## Technical Stack
### 1. **Groq**:
   - Extracts structured job descriptions from unstructured data on the careers page.

### 2. **LangChain**:
   - Constructs the email template dynamically.
   - Matches job descriptions with relevant portfolio links from the vector database.

### 3. **Streamlit**:
   - Provides a user-friendly interface for inputting URLs and managing generated emails.

### 4. **Vector Database**:
   - Stores portfolio data for semantic search and matching (e.g., ChromaDB).

---

## Workflow
1. **User Input**:
   - The user enters the URL of the target company's careers page.

2. **Data Extraction**:
   - Job postings are scraped and parsed into structured JSON using Groq and LangChain.

3. **Portfolio Matching**:
   - For each job posting, the tool queries the vector database for portfolio links that best match the job requirements.

4. **Email Generation**:
   - Personalized cold emails are generated based on the extracted job descriptions and matched portfolio links.

5. **Output**:
   - Emails are displayed in the Streamlit app and can be copied or downloaded.

---

## Example Output
### Input:
- URL: `https://jobs.nike.com`

### Extracted Job Listing:
```json
{
  "role": "Principal Software Engineer",
  "experience": "10+ years in software development",
  "skills": ["Cloud Development", "Microservices Architecture", "Java", "Kubernetes", "CI/CD"],
  "description": "Lead the design and development of scalable software solutions for Nike’s global operations."
}
```

### Matched Portfolio Links:
- Case Study: "Cloud-native Microservices Development for Retail Industry"
- Demo: "Scalable Kubernetes Deployment for E-commerce"

### Generated Email:
**Subject**: Collaborating with Nike for Scalable Software Solutions

**Email Body**:

Dear [Hiring Manager/Team at Nike],

I hope this email finds you well. My name is Mohan, and I am a Business Development Executive at Atliq, a software development company specializing in scalable, cloud-native solutions. I noticed that Nike is currently hiring for a Principal Software Engineer. I wanted to offer a faster and more efficient alternative to meet your needs.

At Atliq, we can provide a dedicated software development engineer with expertise in:
- Cloud Development
- Microservices Architecture
- Kubernetes and CI/CD Pipelines

We recently worked on a project for a retail giant that involved designing and deploying a cloud-native microservices architecture, leading to a 40% increase in system scalability. You can explore the case study here: [Cloud-native Microservices Development for Retail Industry](#).

I’d love to discuss how Atliq can help Nike reduce the time and cost associated with hiring while ensuring top-notch software development expertise. Let me know a convenient time to connect.

Looking forward to your response.

Best regards,  
Mohan  
Business Development Executive  
Atliq Software Solutions  
[Contact Information]

