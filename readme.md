# Cybersecurity Challenges Repository

Welcome to the Cybersecurity Challenges repository! This repository contains a catalogue of cybersecurity scenarios that can be used to help security practitioners sharpen their skills and knowledge in various areas of cybersecurity.

## Scenario Catalogue

The following is a list of the scenarios available in this repository:

1. SQL Injection
2. Broken Authentication and Session Management
3. Cross-Site Scripting (XSS)
4. File Inclusion
5. Command Injection
6. XML External Entity (XXE) Injection
7. Broken Access Control
8. Cross-Site Request Forgery (CSRF)
9. Insecure Cryptographic Storage
10. Insecure Communications
11. Server-Side Request Forgery (SSRF)
12. Remote Code Execution (RCE)
13. Privilege Escalation
14. Buffer Overflow
15. Format String Attack
16. Information Disclosure
17. Clickjacking
18. Insufficient Anti-Automation
19. Malicious File Upload
20. Business Logic Flaws

## Implementation Details

Each scenario in this repository includes a Dockerfile that creates a vulnerable container, which can be used to practice and test your skills. The Dockerfiles are designed to run in a Docker environment, which allows you to easily spin up and tear down containers as

```docker build -t <image-name> .```

This will build a Docker image based on the Dockerfile in the directory. You can then run the container using the following command:



```docker run -p <port>:80 <image-name>```

Replace `<image-name>` with a name for the Docker image, and `<port>` with the port you wish to use for the container.

Each scenario also includes a detailed description of the vulnerability being exploited and tips for how to successfully complete the challenge. We've also included hidden clues and Easter eggs throughout the scenarios to keep things interesting and engaging.

## Contributing

We welcome contributions to this repository! If you have an idea for a new scenario, or if you have suggestions for improving an existing scenario, please feel free to open an issue or submit a pull request.

Please note that all scenarios should be based on real-world vulnerabilities and should not contain any malicious code or actions.

## Disclaimer

This repository is intended for educational purposes only. The scenarios included in this repository should only be used in legal and ethical ways, and we are not responsible for any misuse or illegal activities related to the scenarios or the information provided.

We hope that this repository is helpful for security practitioners looking to sharpen their skills and knowledge in various areas of cybersecurity. Good luck, and have fun! 
