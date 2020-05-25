# KeywordFinder-NLP_Model
A Natural Language Processing model implemented in NLTK that can extract key words from a job description.

Data from: https://www.kaggle.com/residentmario/exploring-monster-com-job-postings

## Summary of Model
This NLP model uses a technique called TF/IDF or 'term frequency - inverse document frequency'. In summary, we compute how common a word is across a large dataset (in this case, 20,000+ job postings on monster.com) and in one specific document. If we find a word that is a lot more common in our document than on average, then we expect that word to be a keyword.

### Example
Below is a Yelp software engineer job posting found on Indeed.ca:

    Software Engineer - Backend Infrastructure (Toronto) Yelp’s mission is to connect users with great local businesses. We are an agile team that creates an amazing experience for millions of people and business owners. We are growing our engineering teams to build, experiment and iterate on new product offerings and improve user experience. One of our challenges is to assist our high velocity engineering teams with speedy delivery of quality products to our users.

    We are looking for tenacious and driven engineers to join our Engineering Effectiveness teams. Our mission is to help developers ship products quickly, reliably and securely and to provide them with the infrastructure they need to build robust and scalable features for our millions of users. We’ve evolved our service oriented architecture, developed API infrastructure for our mobile apps, built scalable CI/CD platforms and continue to do more. We also build tools to analyze tests and surface effectiveness health metrics for all engineering teams at Yelp. We support hundreds of microservices, thousands of docker containers and hundreds of developers.

    As an engineer in Engineering Effectiveness, you will be working closely with the rest of engineering to take on problems of scale and efficiency. Yelp engineering culture is driven by our values: we’re a cooperative team that values individual authenticity, and encourages “unboring” solutions to problems.
    What You Will Do:

    Design, build and deploy scalable and reliable infrastructure for backend services and APIs.
    Support and improve our tools for continuous build, automated testing, source control, and release management.
    Rapidly deliver and maintain high-performance, scalable systems, tools and processes to meet the needs of our rapidly growing engineering teams.
    Work closely with other engineers within your group and across the engineering organization.

    What We Are Looking For:

    Experience designing scalable infrastructure and backend systems, with an understanding of operational and reliability trade-offs.
    Familiarity with containerization technologies such as Docker, Kubernetes etc. and knowledge of distributed systems.
    Proficient in one of Python, Java, C++, or Go.
    Excellent interpersonal and communication skills.
    3+ years of relevant industry experience, if you have less than 1 year of experience please consider applying for our New Grad positions.
    We are open to remote employees for this role.


    Yelp values diversity. We’re proud to be an equal opportunity employer and consider qualified applicants without regard to race, color, religion, sex, national origin, ancestry, age, genetic information, sexual orientation, gender identity, marital or family status, veteran status, medical condition or disability.

    Note: Yelp does not accept agency resumes. Please do not forward resumes to any recruiting alias or employee. Yelp is not responsible for any fees related to unsolicited resumes."""

Using this model, we can extract the following keywords and their TF/IDF scores:


Word           | TF/IDF Score
-------------  | -------------
'scalable'     | 0.4
'engineering'  | 0.347
'infrastructure' | 0.274
'backend' | 0.27
'docker' | 0.212
'build' |  0.195
'effectiveness' | 0.176
'rapidly' | 0.122
'securely' | 0.102
'velocity' | 0.101

Make sure you include these key words in your resume when applying!

## Next Steps

1. Build RESTful API that can take job posting URL/job description and return keywords.
2. Build client (website or Chrome extension) to allow users to quickly generate keywords.
