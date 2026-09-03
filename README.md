<picture>
  <source media="(prefers-color-scheme: dark)" srcset="pipeline-dark.svg">
  <img alt="Ousmane Sanokho, Cloud Engineering student in Kuala Lumpur, building around AWS, infrastructure and reliability" src="pipeline-light.svg" width="880">
</picture>

Second-year BSc (Hons) Information Technology, Cloud Engineering at Asia Pacific University.

I'm still learning most of this. The way I do it is to build something small, break it on purpose, and read the logs until I understand what actually happened.

### What I'm building

**[deployguard](https://github.com/OusmaneSanokho/deployguard)** &nbsp;·&nbsp; working on this now  
AWS infrastructure and delivery pipeline, entirely in Terraform. 44 resources, no credentials stored anywhere, and a bad deploy rolls itself back.  
`Terraform` `AWS` `ECS Fargate` `RDS` `GitHub OIDC`

**[cloudrescue](https://github.com/OusmaneSanokho/cloudrescue)**  
Service monitoring with bounded automatic recovery, written from scratch rather than assembled from Prometheus and Grafana.  
`Python` `Flask` `Docker Compose` `AWS EC2`

**[ai-internship-copilot](https://github.com/OusmaneSanokho/ai-internship-copilot)** &nbsp;·&nbsp; [live](https://ai-internship-copilot-rho.vercel.app)  
CV analyser for students applying to internships. Upload a PDF, get a structured report back.  
`Next.js` `TypeScript` `Claude API` `Supabase`

Newest first. Each one came out of a question the last one left me with: build it, then operate it, then work out how to get it there safely.

<details>
<summary><b>Three things I broke on purpose</b></summary>

<br>

**Removed the ECS role's permission to read the database password.** New tasks refused to start. The already-running one kept serving traffic, because it had resolved its secret before I took the permission away.

**Put the permission back and redeployed straight away.** Two more deploys failed first. IAM is eventually consistent, and I found that out by being impatient.

**Watched CloudRescue log a recovery that never happened.** Its restart call spawns a process inside the monitor's own container, not the app's. The logs said recovered. The outage was still there.

</details>

### What I'm learning

AWS architecture, Terraform module design, reliability, CI/CD, cloud security.

Studying for the AWS Solutions Architect – Associate. Not taken yet.

### Working with

AWS, Terraform, Docker, GitHub Actions  
Python, TypeScript, SQL, Bash  
FastAPI, Flask, Next.js, PostgreSQL, Linux

Looking for a 4–6 month Cloud / DevOps / SRE internship starting January 2027.

[LinkedIn](https://www.linkedin.com/in/ousmane-sanokho-8b05703a7)
