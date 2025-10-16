# How to Create Additional Service Pages

I've created the Software Testing service page as a template. You can easily create the remaining service pages by copying and modifying it.

## Quick Steps:

1. **Copy the template:**
   ```bash
   cp services/software-testing.html services/penetration-testing.html
   ```

2. **Update these sections in the new file:**
   - Page title (line 6)
   - Hero H1 title
   - Hero description paragraph
   - Service navigation links
   - Sub-service sections with IDs

## Remaining Services to Create:

### 1. Penetration Testing (`services/penetration-testing.html`)
**Sub-services:**
- Web Application Testing (#web-app)
- Network Penetration Testing (#network)
- Mobile App Security (#mobile)
- API Security Testing (#api)
- Cloud Security Testing (#cloud)
- Wireless Network Testing (#wireless)

### 2. Red Team Operations (`services/red-team.html`)
**Sub-services:**
- Adversary Simulation (#adversary)
- Social Engineering (#social-engineering)
- Physical Security Testing (#physical)
- Incident Response Testing (#incident-response)
- Purple Team Exercises (#purple-team)
- Threat Intelligence Integration (#threat-intel)

### 3. Security Assessment (`services/security-assessment.html`)
**Sub-services:**
- Vulnerability Assessments (#vulnerability)
- Compliance Audits (#compliance)
- Security Posture Reviews (#posture)
- Risk Analysis (#risk)
- Architecture Review (#architecture)
- Code Security Review (#code-review)

### 4. Security Training (`services/security-training.html`)
**Sub-services:**
- Security Awareness Training (#awareness)
- Secure Coding Workshops (#secure-coding)
- Incident Response Training (#ir-training)
- Custom Training Programs (#custom)
- Phishing Simulation (#phishing)
- Security Certification Prep (#certification)

### 5. Security Consulting (`services/security-consulting.html`)
**Sub-services:**
- Security Strategy (#strategy)
- Architecture Review (#arch-review)
- Security Roadmaps (#roadmap)
- Policy Development (#policy)
- Compliance Consulting (#compliance-consulting)
- CISO Advisory Services (#ciso)

## Content Template for Each Sub-Service:

```html
<div id="sub-service-id" class="sub-service">
    <h2>Sub-Service Name</h2>
    <p>Brief description of what this service provides and why it's important.</p>

    <h3>What We Cover:</h3>
    <ul>
        <li>Key area 1</li>
        <li>Key area 2</li>
        <li>Key area 3</li>
        <li>Key area 4</li>
    </ul>

    <h3>Deliverables:</h3>
    <ul>
        <li>Report 1</li>
        <li>Report 2</li>
        <li>Documentation</li>
    </ul>
</div>
```

## After Creating All Service Pages:

Update the homepage service cards to link to these pages. In `index.html`, change:

```html
<!-- OLD -->
<div class="service-card">
    <div class="service-icon">🔍</div>
    <h3>Software Testing</h3>
    ...
</div>

<!-- NEW -->
<div class="service-card">
    <a href="services/software-testing.html" style="text-decoration: none; color: inherit;">
        <div class="service-icon">🔍</div>
        <h3>Software Testing</h3>
        ...
    </a>
</div>
```

Or wrap just the title:
```html
<h3><a href="services/software-testing.html">Software Testing</a></h3>
```

## SEO Benefits:

- Each service gets its own dedicated page
- Deep linking to specific sub-services
- Better keyword targeting
- More content for search engines to index
- Clear site structure

## Quick Command to Create All Files:

```bash
cd services
for service in "penetration-testing" "red-team" "security-assessment" "security-training" "security-consulting"; do
    cp software-testing.html $service.html
done
```

Then edit each file with the appropriate content!
