
### Control of artifacts, dependencies, and images

> <details>
> <summary>Management and control of external component usage [T-ADI-DEP]</summary>
>
> | ID | Practices | DAF maturity pyramid level | BSIMMv14 | DSOMM | SAMMv2 | 
> | --- | --- | --- | --- | --- | --- |
> | T-ADI-DEP-1-1 | There are (formalized) unified rules that define whether certain dependencies can be used in the code.</br>For example, there is an approved document and/or a knowledge base page describing the procedure for using dependencies in the code. | 2 | - | - | SB-B-2 |
> | T-ADI-DEP-1-2 | Updates to the existing dependencies are performed manually.</br>For example, when a new version of a library is required, you must manually download it and add it to the project. | 2 | - | 9 | SB-B-2  |
> | T-ADI-DEP-1-3 | A documented and formalized response plan for information security incidents related to dependencies exists. | 2 | SR2.7 | - | - |
> | T-ADI-DEP-1-4 | Hardening (secure configuration) of configuration files for the open-source software (OSS) packages in use (e.g., nuget.config, .npmrc, pip.conf, pom.xml, etc.) is performed. | 2 | - | 83, 91, 56 | EM-A-1 |
> | T-ADI-DEP-1-5 | Dependencies with the “latest” tag are not used. | 2 | - | - | SA-B-1 |
> | T-ADI-DEP-2-1 | Developers obtain and use OSS components exclusively through standardized (formalized and approved) methods. | 3 | SR2.7 | - | - |
> | T-ADI-DEP-2-2 | The use of newly released (less than 60 days old) and outdated (more than 365 days old) OSS components is monitored and regulated.</br>For example, an OSS firewall is configured to issue warnings (or block) when attempting to use OSS that was released or updated more than 365 days ago or less than 60 days ago. | 3 | - | - | OM-B-1, OM-B-2, SB-B-2 |
> | T-ADI-DEP-3-1 | An inventory of the dependencies in use is maintained.</br>For example, an internal repository or knowledge base has been established for this purpose. | 4 | SR1.5 | - | SB-B-1 |
> | T-ADI-DEP-3-2 | When a Pull/Merge request is created, a list of all vulnerabilities in the dependencies used must be provided.</br>This can be implemented by means of an SCA solution. | 4 | - | - | - |
> | T-ADI-DEP-3-3 | Automatic updating of the dependencies in use is implemented.</br>This can be achieved using specialized dependency update utilities. | 4 | - | 10 | - |
> | T-ADI-DEP-4-1 | Verification of the digital signature of the SBOM is performed prior to using dependencies in the build.</br>The Verification of the SBOM digital signature is performed prior to using dependencies in the build. This can be implemented using an SCA  | 6 | - | - | - |
> | T-ADI-DEP-4-2 | Required dependencies are built independently in a trusted environment. | 6 | - | - | - |
> </details>

> <details>
> <summary>Management and control of application development artifacts [T-ADI-ART]</summary>
>
> | ID | Practices | DAF maturity pyramid level | BSIMMv14 | DSOMM | SAMMv2 | 
> | --- | --- | --- | --- | --- | --- |
> | T-ADI-ART-1-1 | Artifact management is present in some form | 1 | - | - | - |
> | T-ADI-ART-1-2 | All development artifacts are stored in trusted registries.</br>For example, an internal registry is used. | 1 | - | 60, 58, 57 | - |
> | T-ADI-ART-1-3 | External services are used for authentication in the registry.</br>For example, integration with a LDAP/SAML system is in place, and local accounts are not used. | 1 | - | 60, 59 | - |
> | T-ADI-ART-1-4 | Anonymous access to the registry is disabled | 1 | - | - | - |
> | T-ADI-ART-1-5 | Auditing of all configuration changes to artifact repositories is configured and enabled | 1 | - | 108, 106, 101 | - |
> | T-ADI-ART-2-1 | Developers obtain artifacts for further work exclusively from internal repositories | 3 | - | - | - |
> | T-ADI-ART-2-2 | Webhooks use TLS version 1.2 or higher for interactions with the registry | 3 | - | - | - |
> | T-ADI-ART-3-1 | An SBOM is created for all artifacts | 4 | SR1.5, SE3.6 | 4 | - |
> | T-ADI-ART-3-2 | Multi-factor authentication is used to access the registry. | 4 | - | 60, 59 | - |
> | T-ADI-ART-4-1 | The build pipeline signs all artifacts it creates. | 5 | SE2.4 | - | - |
> | T-ADI-ART-4-2 | All artifacts in the registry are encrypted. | 5 | - | - | - |
> | T-ADI-ART-4-3 | Digital signatures are created for all artifacts after security checks have been completed and before they are uploaded to the trusted registry. | 5 | SE2.4 | - | - |
> | T-ADI-ART-4-4 | Hash sums are generated for all artifacts before they are uploaded to the registry and verified during the build process. | 5 | - | - | - |
> </details>


### Development environment security

> <details>
> <summary>Developers workstations security [T-DEV-COMP]</summary>
>
> | ID | Practices | DAF maturity pyramid level | BSIMMv14 | DSOMM | SAMMv2 | 
> | --- | --- | --- | --- | --- | --- |
> | T-DEV-COMP-1-1 | Baseline requirements for software and configurations on corporate developer workstations are approved and applied.</br>For example, requirements for antivirus, operating system updates, and password policies. | 1 | - | - | - |
> | T-DEV-COMP-1-2 | Remote access to development tools from non-corporate (non-hardened) devices is permitted for only a small, limited number of devices. | 1 | - | - | - |
> | T-DEV-COMP-2-1 | Remote access to development tools is only allowed either from corporate devices managed through MDM or via intermediary/proxy systems such as VDI or PAM. | 3 | - | - | - |
> </details>

> <details>
> <summary>Secrets management in DEV/TEST environments [T-DEV-SM]</summary>
>
> | ID | Practices | DAF maturity pyramid level | BSIMMv14 | DSOMM | SAMMv2 | 
> | --- | --- | --- | --- | --- | --- |
> | T-DEV-SM-1-1 | Secrets in the development environment are protected using the built-in mechanisms of development tools (e.g., CI/CD systems), without the use of dedicated secret management systems. | 1 | - | 7 | SD-B-1 |
> | T-DEV-SM-1-2 | Information security incidents related to the use of secrets in the development environment are handled by the Information Security team in cooperation with the developers. | 1 | CMVM1.1 | - | IM-A-2  |
> | T-DEV-SM-2-1 | Secrets in the development environment are stored in a secret management tool, such as HashiCorp Vault. | 2 | - | 7 | SD-B-2 |
> | T-DEV-SM-2-2 | Developers and engineers exchange secrets using a secret management tool, such as HashiCorp Vault. | 2 | - | - | SD-B-2 |
> | T-DEV-SM-3-1 | Secrets of all environments and tools (excluding developer workstations and similar ad-hoc environments) are stored in a secret management system (e.g., Vault). The number of hardcoded secrets is kept to a minimum. The cases where hardcoded secrets are used are known to the Information Security team, and a plan is in place to phase them out. | 3 | - | 7 | SD-B-1 |
> | T-DEV-SM-3-2 | A secret rotation policy for development environments has been established and is applied | 3 | - | - | SD-B-3 |
> | T-DEV-SM-4-1 | Dynamic, access-restricted secrets are used for environments. | 6 | - | - | - |
> </details>

> <details>
> <summary>Build-environment security [T-DEV-BLD]</summary>
>
> | ID | Practices | DAF maturity pyramid level | BSIMMv14 | DSOMM | SAMMv2 | 
> | --- | --- | --- | --- | --- | --- |
> | T-DEV-BLD-1-1 | Access to the build environment (orchestrator, worker nodes, etc.) is restricted via RBAC configuration. | 2 | - | 57, 58 | - |
> | T-DEV-BLD-1-2 | A push approach (rarther than pull) is used to deliver parameters to all build worker nodes. | 2 | - | - | - |
> | T-DEV-BLD-1-3 | Each build worker node has only the minimum required network access (restricted to necessary services and limited to specific ports and protocols). | 2 | - | - | SB-A-2 |
> | T-DEV-BLD-1-4 | Centralized storage of build logs, including configuration changes, is implemented. | 2 | - | - | SB-A-3 |
> | T-DEV-BLD-2-1 | Monitoring and incident response are implemented for build worker nodes in reagrds to the consumption of computing resources (CPU, RAM, HDD, etc.). | 3 | CMVM1.1 | - | - |
> | T-DEV-BLD-3-1 | Each build worker node has a dedicated role (e.g., testing, compilation, artifact delivery), and no other tasks are executed on it. | 5 | - | 3 | - |
> | T-DEV-BLD-3-2 | Security hardening standards are applied to build worker nodes. | 5 | - | 83, 56 | SB-A-1, SB-A-2 |
> | T-DEV-BLD-3-3 | All build worker node configurations are centrally stored in the source code management system. | 5 | - | - | - |
> | T-DEV-BLD-4-1 | The creation of the build environment is automated using Infrastructure as Code (IaC). | 6 | - | 3 | - |
> </details>

> <details>
> <summary>Source code management system (SCM) security [T-DEV-SCM]</summary>
>
> | ID | Practices | DAF maturity pyramid level | BSIMMv14 | DSOMM | SAMMv2 | 
> | --- | --- | --- | --- | --- | --- |
> | T-DEV-SCM-1-1 | Only designated users (e.g., configured through RBAC) have permissions to create and delete repositories. | 2 | - | 57 | - |
> | T-DEV-SCM-1-2 | Only designated users (e.g., configured through RBAC) have permissions to can delete issues. | 2 | - | - | - |
> | T-DEV-SCM-1-3 | Only designated users (e.g., configured through RBAC) have permissions to can create teams or groups. | 2 | - | - | - |
> | T-DEV-SCM-1-4 | The number of SCM administrators is limited and reviewed regularly. | 2 | - | - | - |
> | T-DEV-SCM-1-5 | Access to the version control system is managed through a role-based model built on the principle of least privilege. The model regulates at minimum:</br>- The ability to create repositories</br>- The ability to delete repositories</br>- The ability to modify repository visibility | 2 | - | - | - |
> | T-DEV-SCM-1-6 | Regular users are allowed to create only private repositories. | 2 | - | - | - |
> | T-DEV-SCM-1-7 | Administrator approval is required for the installation of any applications or extensions in Source Code Management (SCM) systems. | 2 | - | - | - |
> | T-DEV-SCM-2-1 | Auditing is enabled for all code forks, and a responsible owner is assigned. | 3 | - | - | - |
> | T-DEV-SCM-2-2 | A regular process is in place to identify, review, and remove inactive users from all projects. | 3 | - | - | - |
> | T-DEV-SCM-2-3 | Email notifications can be sent only to trusted (verified) domains. | 3 | - | - | - |
> | T-DEV-SCM-2-4 | Inactive (unnecessary) applications (such as plugins or extensions) are removed from the SCM system. | 3 | - | - | OM-B-1 |
> | T-DEV-SCM-2-5 | Each repository is configured by default with minimum user privileges. | 3 | - | - | SA-A-1 |
> | T-DEV-SCM-2-6 | Only corporate email addresses are used when adding new users to the SCM system. | 3 | - | - | - |
> | T-DEV-SCM-3-1 | All changes to project visibility are tracked. | 4 | - | - | - |
> | T-DEV-SCM-3-2 | Unused repositories are identified and archived on a regular basis | 4 | - | - | - |
> | T-DEV-SCM-3-3 | Access to the SCM system is carried out using multi-factor authentication. | 4 | - | 59, 60 | - |
> | T-DEV-SCM-3-4 | Access to SCM systems is allowed only from authorized IP addresses. | 4 | - | - | - |
> | T-DEV-SCM-4-1 | Code is analyzed for anomalies relevant to the organization (for example, a commit contains disproportionately large code changes or an excessive number of commits occur within a short period). | 6 | - | - | - |
> | T-DEV-SCM-4-2 | Access for developers to repositories is performed using certificates issued exclusively by the company’s internal Certification Authority (CA), not self-signed certificates, as an additional authentication factor. | 6 | - | - | - |
> | T-DEV-SCM-4-3 | Automated hardening of SCM project settings is implemented via APIs or developer platform engineering, with regular state comparison. | 6 | - | - | - |
> </details>

> <details>
> <summary>Source code change management and control [T-DEV-SRC]</summary>
>
> | ID | Practices | DAF maturity pyramid level | BSIMMv14 | DSOMM | SAMMv2 | 
> | --- | --- | --- | --- | --- | --- |
> | T-DEV-SRC-1-1 | All changes to source code are tracked using a version control system (SCM). | 1 | - | - | - |
> | T-DEV-SRC-1-2 | The review cycle for a source code merge request is reinitiated when additional changes are proposed. | 1 | - | - | - |
> | T-DEV-SRC-1-3 | Developers do not have “dismiss code change review” permissions, which would allow them to bypass the standard code review procedure. | 1 | - | - | - |
> | T-DEV-SRC-1-4 | For all repositories, the linear history option is enabled. Only squash and rebase merge options are available. | 1 | - | - | - |
> | T-DEV-SRC-1-5 | Branch protection is enforced for all repositories to prevent unauthorized or uncontrolled changes to protected branches. | 1 | - | - | - |
> | T-DEV-SRC-2-1 | Unused branches are regularly analyzed and removed. | 3 | - | - | - |
> | T-DEV-SRC-2-2 | A merge request is finalized only after all checks have successfully passed. | 3 | ST3.6 | 68 | - |
> | T-DEV-SRC-2-3 | Before a merge request is submitted, all open branches must be updated to the latest state to ensure consistency and prevent conflicts. | 3 | - | - | - |
> | T-DEV-SRC-2-4 | Merging of source code changes is allowed only when there are no open comments or discussions. | 3 | - | - | - |
> | T-DEV-SRC-2-5 | Each source code change has a corresponding ticket in the task management system (e.g., Jira). | 3 | - | - | - |
> | T-DEV-SRC-2-6 | Branch protection rules are applied to administrator accounts as well. | 3 | - | 65 | - |
> | T-DEV-SRC-3-1 | Code Owners are defined and assigned for the most critical files. | 4 | - | - | - |
> | T-DEV-SRC-3-2 | Code Owners approve changes to the files they are responsible for. | 4 | - | - | - |
> | T-DEV-SRC-3-3 | Merge requests  contain only signed commits. Unsigned commits are not permitted under any circumstances, especially for the main branch. | 4 | SE2.4 | - | - |
> | T-DEV-SRC-3-4 | Every merge request  undergoes approval from at least two authenticated users before it can be finalized, ensuring accountability and reducing the risk of unauthorized changes. | 4 | - | - | - |
> | T-DEV-SRC-3-5 | All attempts to delete protected branches are monitored and logged, with alerts generated for the Information Security team to ensure accountability and prevent unauthorized removal | 4 | - | - | - |
> | T-DEV-SRC-3-6 | The use of ‘skip/ignore scan’ inline comments and ignore configuration files (e.g., .aiignore, .gitleaksignore) by security scanners (SAST, SCA, Secrets) is strictly monitored. | 4 | - | 68 | - |
> | T-DEV-SRC-4-1 | For all repositories, the “force push” function is available only to the owner. | 6 | - | 63 | - |
> </details>

> <details>
> <summary>Build pipeline security [T-DEV-CICD]</summary>
>
> | ID | Practices | DAF maturity pyramid level | BSIMMv14 | DSOMM | SAMMv2 | 
> | --- | --- | --- | --- | --- | --- |
> | T-DEV-CICD-1-1 | Access to the build pipeline is restricted, with RBAC configured. | 1 | - | - | - |
> | T-DEV-CICD-1-2 | Event logs of build pipelines are centrally stored. | 1 | - | - | - |
> | T-DEV-CICD-1-3 | A “CI/CD as Code” approach is used for pipeline creation. | 1 | SM3.4 | - | - |
> | T-DEV-CICD-1-4 | Protected tags (tag protection) are enforced. | 1 | - | - | - |
> | T-DEV-CICD-1-5 | Use of [skip ci] directives and pre-commit hooks to bypass pipeline execution is prohibited. | 1 | - | - | - |
> | T-DEV-CICD-2-1 | For each build stage, input and output parameters and results are strictly defined. | 3 | - | - | - |
> | T-DEV-CICD-2-2 | Changes to CI/CD configuration files (build pipelines) are continuously tracked. | 3 | - | - | - |
> | T-DEV-CICD-3-1 | All Build-stage logs are centrally stored. | 4 | - | - | - |
> | T-DEV-CICD-4-1 | Each CI/CD pipeline used for builds is single-purpose (e.g., testing, compilation, artifact delivery); no other tasks are executed on it. | 5 | - | - | - |
> </details>


### Tool-Based security defects detection and analysis

> <details>
> <summary>Security assurance for vendor-developed software [T-CODE-SPC]</summary>
>
> | ID | Practices | DAF maturity pyramid level | BSIMMv14 | DSOMM | SAMMv2 | 
> | --- | --- | --- | --- | --- | --- |
> | T-CODE-SPC-1-1 | Baseline information security functional requirements for contractor-developed software are established. | 2 | - | - | - |
> | T-CODE-SPC-1-2 | When selecting a contractor for custom development, its capabilities, experience, and existing secure development practices are taken into account. | 2 | - | - | - |
> | T-CODE-SPC-2-1 | For critical applications developed by contractors, penetration testing is performed regularly and/or source code is reviewed internally or by specialized contractors. | 4 | - | - | - |
> | T-CODE-SPC-2-2 | Detailed cybersecurity requirements for the application development process are defined and taken into account during contractor selection, including:</br>- requirements for the availability and use of code and component analyzers (e.g., SAST/SCA) during development;</br>- requirements for providing reports demonstrating the absence and/or remediation of identified vulnerabilities in the software under development;</br>- other relevant criteria. | 4 | - | - | - |
> | T-CODE-SPC-2-3 | Procedures for identifying vulnerabilities and tracking their remediation in contractor-developed software are developed and enforced within the company. | 4 | - | - | - |
> | T-CODE-SPC-2-4 | Application development contracts include provisions requiring an SBOM for each software version, with defined mechanisms for obtaining it. | 4 | - | - | - |
> | T-CODE-SPC-3-1 | Composition analysis (SCA) of contractor-developed custom software is performed within the customer company. | 5 | - | - | - |
> | T-CODE-SPC-3-2 | For all contractor-developed applications, penetration testing is conducted; where source code is provided, it is reviewed internally or by specialized contractors | 5 | - | - | - |
> | T-CODE-SPC-3-3 | All artifacts delivered by the contractor (including the SBOM) are digitally signed, and a process for verifying the signatures of delivered artifacts is implemented | 5 | - | - | - |
> | T-CODE-SPC-3-4 | Development contracts require delivery of the complete, buildable source code and associated files (e.g., build scripts, configuration, and dependencies). | 5 | - | - | - |
> | T-CODE-SPC-3-5 | Static analysis (SAST) is performed on supplier-developed source code, and the findings are reviewed | 5 | - | - | - |
> | T-CODE-SPC-4-1 | All contractor-developed software is built within the customer’s infrastructure, using the full suite of secure development tools and following the customer’s processes. | 7 | - | - | - |
> </details>

> <details>
> <summary>Static application security testing (SAST) [T-CODE-SST]</summary>
>
> | ID | Practices | DAF maturity pyramid level | BSIMMv14 | DSOMM | SAMMv2 | 
> | --- | --- | --- | --- | --- | --- |
> | T-CODE-SST-1-1 | Source code analysis is applied, at minimum, on an ad-hoc basis. | 2 | CR1.2 | - | ST-A-1 |
> | T-CODE-SST-1-2 | At minimum, default SAST rules are used. | 2 | - | - | ST-A-1 |
> | T-CODE-SST-2-1 | Regular scanning of specific code portions is performed, for example:</br>-Changes made following sprint results;</br>-Code of internally developed frameworks; | 3 | - | 174, 175, 176 | ST-A-2 |
> | T-CODE-SST-2-2 | Unused SAST analysis rules are disabled. | 3 | - | - | ST-A-2 |
> | T-CODE-SST-2-3 | SAST is integrated into CI (a separate script is used for each development team). | 3 | SM3.4, CR1.4, CR1.5 | - | ST-A-3 |
> | T-CODE-SST-2-4 | SAST IDE plugins are used (where available). | 3 | - | - | - |
> | T-CODE-SST-3-1 | Regular SAST scanning of the entire codebase is performed. | 4 | - | - | ST-A-1 |
> | T-CODE-SST-3-2 | Customized rules are used. | 4 | CR2.6 | - | ST-A-2 |
> | T-CODE-SST-3-3 | SAST is integrated with the code-quality tool (e.g., SonarQube). | 4 | - | - | - |
> | T-CODE-SST-4-1 | Source code of open-source components is scanned (for malware, protestware, etc.). | 7 | - | 173 | SB-B-3 |
> </details>

> <details>
> <summary>Software Composition Analysis/Open Source Analysis (SCA/OSA) [T-CODE-SC]</summary>
>
> | ID | Practices | DAF maturity pyramid level | BSIMMv14 | DSOMM | SAMMv2 | 
> | --- | --- | --- | --- | --- | --- |
> | T-CODE-SC-1-1 | SCA scanner uses the default rule set. | 1 | SE3.8 | - | - |
> | T-CODE-SC-1-2 | Selective manual blocking of dependencies is applied when serious security defects are identified. | 1 | - | - | - |
> | T-CODE-SC-1-3 | A complete history of all libraries used is retained in SCA. | 1 | SR1.5 | - | - |
> | T-CODE-SC-2-1 | High-severity vulnerable libraries, including those with RCE, are blocked by agreement between Information Security Department and the development team. | 2 | - | - | DM-A-2 |
> | T-CODE-SC-2-2 | The acquisition of images is controlled, with retrieval limited to trusted repositories. | 2 | - | - | - |
> | T-CODE-SC-2-3 | Verification of components’ digital signatures and hashes is performed. | 2 | SE2.4 | - | SB-A-1 |
> | T-CODE-SC-2-4 | SCA scanner is integrated into CI/CD. | 2 | SM3.4, CR1.4, CR1.5 | - | ST-A-3 |
> | T-CODE-SC-2-5 | License-compliance checks are performed using SCA tool. | 2 | SR2.7 | - | SB-B-2 |
> | T-CODE-SC-3-1 | All available open-source feeds are integrated into the SCA solution | 4 | - | - | - |
> | T-CODE-SC-3-2 | Combined SAST and SCA practices are applied to identify code vulnerabilities through effective-usage analysis (e.g., a library is vulnerable, but the vulnerable method is not used). | 4 | CR3.2 | 161 | - |
> | T-CODE-SC-3-3 | SCA IDE plugins are used for pre-commit Git hooks | 4 | - | - | - |
> | T-CODE-SC-3-4 | End-of-life libraries are blocked by agreement between Information Security team and developers. | 4 | - | - | OM-B-2 |
> | T-CODE-SC-4-1 | Paid enrichment feeds are used to augment analysis results for open-source components. | 6 | - | - | - |
> </details>

> <details>
> <summary>Image container security analysis [T-CODE-IMG]</summary>
>
> | ID | Practices | DAF maturity pyramid level | BSIMMv14 | DSOMM | SAMMv2 | 
> | --- | --- | --- | --- | --- | --- |
> | T-CODE-IMG-1-1 | Container image vulnerability scanning is performed using a standardized toolset across all development teams | 1 | - | - | - |
> | T-CODE-IMG-1-2 | The image scans are performed manually. | 1 | - | - | - |
> | T-CODE-IMG-1-3 | Selective manual blocking of container images is applied when critical security defects are discovered in the image. | 1 | - | - | - |
> | T-CODE-IMG-2-1 | Container image vulnerability scanning is integrated into CI/CD. | 2 | SM3.4 | - | - |
> | T-CODE-IMG-2-2 | Container images stored in internal repositories are periodically scanned for vulnerabilities. | 2 | - | - | - |
> | T-CODE-IMG-2-3 | When critical security defects are detected in container images, tickets are automatically created for remediation. | 2 | - | - | - |
> | T-CODE-IMG-3-1 | Non-compliant container images are blocked as agreed by the Information Security and development teams. | 3 | SE2.4 | - | - |
> | T-CODE-IMG-4-1 | Verification of container image digital signatures is performed. | 4 | - | - | - |
> | T-CODE-IMG-4-2 | CI/CD builds are blocked when high-severity vulnerabilities are found in container images, in coordination between the Information Security and development teams. | 4 | - | - | - |
> </details>

> <details>
> <summary>Secrets detection [T-CODE-SECDN]</summary>
>
> | ID | Practices | DAF maturity pyramid level | BSIMMv14 | DSOMM | SAMMv2 | 
> | --- | --- | --- | --- | --- | --- |
> | T-CODE-SECDN-1-1 | Secret detection mechanisms are applied at least in SCM systems. | 1 | - | 131 | - |
> | T-CODE-SECDN-1-2 | Secret detection tools are run manually (ad hoc). | 1 | - | - | - |
> | T-CODE-SECDN-1-3 | Secret detection tools use default scanning settings. | 1 | - | - | - |
> | T-CODE-SECDN-1-4 | Security incidents involving discovered secrets are resolved jointly between Information Security and the development teams. | 1 | CMVM1.1 | - | IM-A-2 |
> | T-CODE-SECDN-2-1 | Secret detection tools cover:</br>- all versions of code stored in SCM;</br>- IaC manifests;</br>- artifacts, including Docker images;</br>- all repositories;</br>- cloud infrastructure;</br>- scanning and blocking of secrets during pull/Merge stages. | 2 | - | 131 | - |
> | T-CODE-SECDN-2-2 | Fine-tuned configurations are used for secret-scanning tools | 2 | CR2.6 | - | - |
> | T-CODE-SECDN-2-3 | Prioritization is applied when handling security events related to discovered secrets. | 2 | - | - | IM-B-2 |
> | T-CODE-SECDN-3-1 | Commits containing secrets are blocked in coordination between Information Security and the development team. | 3 | - | - | - |
> | T-CODE-SECDN-3-2 | Secret scanning also covers:</br>- developer workstations and ad-hoc environments;</br>- build logs. | 3 | - | - | - |
> | T-CODE-SECDN-3-3 | Secrets auto-validation tools are used. | 3 | - | - | - |
> | T-CODE-SECDN-4-1 | No hardcoded secrets are present in the environment (secret scanning is performed with multiple tools and, over an extended period—e.g., six months—has not identified any hardcoded secrets). | 5 | - | - | SD-B-2 |
> </details>

> <details>
> <summary>Dockerfiles analysis [T-CODE-DOCKERFS]</summary>
>
> | ID | Practices | DAF maturity pyramid level | BSIMMv14 | DSOMM | SAMMv2 | 
> | --- | --- | --- | --- | --- | --- |
> | T-CODE-DOCKERFS-1-1 | A standard for secure Dockerfiles is defined and applied | 1 | - | - | - |
> | T-CODE-DOCKERFS-1-2 | Manual security review of Dockerfiles is performed. | 1 | - | - | - |
> | T-CODE-DOCKERFS-2-1 | Dockerfiles are validated automatically within the CI/CD pipeline | 2 | - | - | - |
> </details>


### Runtime application analysis (Pre-Prod environment)

> <details>
> <summary>Dynamic Application Security testing (DAST) in PREPROD environment [T-PREPROD-DAST]</summary>
>
> | ID | Practices | DAF maturity pyramid level | BSIMMv14 | DSOMM | SAMMv2 | 
> | --- | --- | --- | --- | --- | --- |
> | T-PREPROD-DAST-1-1 | DAST scanning is used at least for the user interface. | 3 | - | 152 | ST-A-1 |
> | T-PREPROD-DAST-1-2 | DAST scanning is performed manually. | 3 | - | - | - |
> | T-PREPROD-DAST-2-1 | DAST rules that are not in use are disabled | 4 | - | - | ST-A-2 |
> | T-PREPROD-DAST-2-2 | Unauthenticated scanning is performed with full UI coverage, including:</br>- spider scanning (e.g., https://www.zaproxy.org/docs/desktop/addons/spider/);</br>- dependency scanning. | 4 | ST1.4 | 122, 123 | - |
> | T-PREPROD-DAST-2-3 | DAST authenticated scans are performed, including:</br>- dependency scanning;</br>- exercising all available roles and user types;</br>- support for existing sessions;</br>- use of log-in/log-out flows;</br>- spider scanning after authentication. | 4 | ST1.4 | - | - |
> | T-PREPROD-DAST-2-4 | DAST vulnerability scanning is integrated into CI/CD. | 4 | - | - | ST-A-3 |
> | T-PREPROD-DAST-3-1 | DAST scanning includes hidden paths. | 5 | - | 123 | - |
> | T-PREPROD-DAST-3-2 | DAST scanners are configured with customized parameters to maximize input-parameter coverage and enhance overall scan breadth | 5 | - | 124 | ST-A-2 |
> | T-PREPROD-DAST-3-3 | DAST scanning includes business-logic paths (e.g., logging in, updating account details, adding items to the cart). | 5 | - | 122 | RT-B-2 |
> | T-PREPROD-DAST-3-4 | Separate DAST scanning of backend and frontend is performed, including:</br>- scanning of SOAP services;</br>- scanning of proxy services that relay requests between frontend and backend;</br>- fuzzing of XML and JSON data sent to API services. | 5 | ST2.6 | - | - |
> | T-PREPROD-DAST-4-1 | Scanning covers all paths and interactions (including with the backend). | 6 | - | 123, 124 | - |
> | T-PREPROD-DAST-4-2 | Use of multiple scanner engines increases coverage and enables cross-validation of results. | 6 | - | 137 | ST-A-1 |
> | T-PREPROD-DAST-4-3 | Custom dynamic-testing profiles are used with increased intensity and rigor for critical parts of the application. | 6 | - | 136 | ST-B-1 |
> </details>

> <details>
> <summary>Pre-Release software penetration testing [T-PREPROD-PENTEST]</summary>
>
> | ID | Practices | DAF maturity pyramid level | BSIMMv14 | DSOMM | SAMMv2 | 
> | --- | --- | --- | --- | --- | --- |
> | T-PREPROD-PENTEST-1-1 | Penetration testing is conducted regularly in the Preprod environment | 1 | - | - | ST-B-2 |
> | T-PREPROD-PENTEST-1-2 | Black-box penetration tests of the Preprod environment are performed (the tester knows only basic information about the target, such as domain names and IP addresses). | 1 | - | - | ST-B-2  |
> | T-PREPROD-PENTEST-1-3 | Gray-box penetration tests are performed (the tester knows the environment architecture and the analyzed software, including versions, and has access to the source code, etc.). | 1 | PT2.2 | - | ST-B-2  |
> | T-PREPROD-PENTEST-2-1 | A documented procedure detailing the methodology and the conditions under which penetration testing is performed in the Preprod environment is defined and applied | 2 | - | - | - |
> | T-PREPROD-PENTEST-4-1 | Security analysis of secure-development tools (e.g., SAST, OSA/SCA) is performed to identify vulnerabilities or defects, including whether reports, configurations, and similar tool artifacts can be accessed without authorization or leveraged by an attacker | 6 | - | - | - |
> </details>

> <details>
> <summary>Functional security testing [T-PREPROD-SECTEST]</summary>
>
> | ID | Practices | DAF maturity pyramid level | BSIMMv14 | DSOMM | SAMMv2 | 
> | --- | --- | --- | --- | --- | --- |
> | T-PREPROD-SECTEST-1-1 | Security features testing is conducted (ad hoc, not formally regulated). | 1 | - | - | RT-A-1 |
> | T-PREPROD-SECTEST-2-1 | A procedure regulating the conduct of functional tests related to security feature is defined and applied. | 2 | ST1.1 | - | PC-A-2 |
> | T-PREPROD-SECTEST-2-2 | At least 5% of functional tests related to security features are automated. | 2 | ST2.5 | - | RT-A-1 |
> | T-PREPROD-SECTEST-3-1 | More than 20% of functional tests related to security featuress are automated. | 6 | ST2.5 | - | RT-A-3 |
> </details>

> <details>
> <summary>Vulnerability management (PREPROD Infrastructure) [T-PREPROD-VULN]</summary>
>
> | ID | Practices | DAF maturity pyramid level | BSIMMv14 | DSOMM | SAMMv2 | 
> | --- | --- | --- | --- | --- | --- |
> | T-PREPROD-VULN-1-1 | Vulnerability scanning of the PREPROD infrastructure is performed periodically in a manual mode using automation tools or scripts (ad hoc, not formally governed). | 2 | - | - | - |
> | T-PREPROD-VULN-1-2 | Infrastructure components are regularly updated, including the remediation of identified vulnerabilities. | 2 | - | 9 | EM-B-2 |
> | T-PREPROD-VULN-2-1 | Regular scanning of the most critical PREPROD infrastructure components for vulnerabilities is performed, and a remediation process is in place. | 4 | - | - | - |
> | T-PREPROD-VULN-2-2 | Regular asset-inventory tasks for PREPROD infrastructure  are performed using automated tools. | 4 | SM3.1, AM2.9 | - | - |
> | T-PREPROD-VULN-2-3 | Security updates are regularly installed on the key PREPROD infrastructure elements (e.g., the orchestrator and server operating systems). | 4 | - | - | EM-B-3 |
> | T-PREPROD-VULN-3-1 | Regular vulnerability scanning of all PREPROD infrastructure components is performed, with an established remediation process. | 5 | - | - | - |
> | T-PREPROD-VULN-3-2 | Automated checks of the main PREPROD infrastructure components (e.g., orchestrator and server operating systems) against best practices are performed, and a process for correcting non-compliance settings is in place. | 5 | - | - | - |
> | T-PREPROD-VULN-3-3 | Regular vulnerability scanning of the PREPROD infrastructure is performed using automated tools in penetration-test mode. | 5 | - | - | - |
> | T-PREPROD-VULN-3-4 | Security updates are regularly installed on all PREPROD infrastructure elements (e.g., the orchestrator and server operating systems). | 5 | - | - | - |
> | T-PREPROD-VULN-4-1 | Automated checks of all PREPROD infrastructure components for compliance with best practices are performed, with a process in place for remediating non-compliance settings. | 7 | - | - | - |
> | T-PREPROD-VULN-4-2 | Regular replacement of vendor-unsupported (outdated) software for PREPROD infrastructure components is performed. | 7 | - | - | OM-B-3 |
> </details>

> <details>
> <summary>Manifests security management (k8s, terraform etc) [T-PREPROD-MANSEC]</summary>
>
> | ID | Practices | DAF maturity pyramid level | BSIMMv14 | DSOMM | SAMMv2 | 
> | --- | --- | --- | --- | --- | --- |
> | T-PREPROD-MANSEC-1-1 | Dockerfiles are analyzed for security defects. | 2 | - | - | - |
> | T-PREPROD-MANSEC-2-1 | Configuration (e.g., Kubernetes, IaC) is checked for security defects. | 3 | SE2.2 | - | - |
> </details>


### Applications & infrastructure security (Runtime in the production environment)

> <details>
> <summary>Secrets management in PROD environment [T-PROD-SM]</summary>
>
> | ID | Practices | DAF maturity pyramid level | BSIMMv14 | DSOMM | SAMMv2 | 
> | --- | --- | --- | --- | --- | --- |
> | T-PROD-SM-1-1 | Built-in software mechanisms are used for secret management (e.g. Gitlab variables). Dedicated secrets-management tools are not used. | 1 | - | 7 | - |
> | T-PROD-SM-1-2 | Security incidents involving secrets are resolved jointly with system owners. | 1 | CMVM1.1 | - | - |
> | T-PROD-SM-2-1 | Secrets management tools are used, but their use is not formally governed. | 2 | - | 7 | - |
> | T-PROD-SM-2-2 | Prioritization of security incidents related to secrets is applied (e.g., event A is assigned a higher priority than event B); prioritization rules are formalized. | 2 | - | - | - |
> | T-PROD-SM-3-1 | Secrets for all environments (except Dev) are stored in a secrets management system; situational use of hardcoded secrets is tolerated. | 3 | - | - | - |
> | T-PROD-SM-3-2 | Automated rotation of all secrets is defined and performed—both on a schedule and on event/request. | 3 | - | - | - |
> | T-PROD-SM-3-3 | Procedures governing the use of secrets management tools are developed and applied. | 3 | - | - | - |
> | T-PROD-SM-4-1 | Dynamic secrets are used and generated for each system-to-system interaction session. | 5 | - | - | - |
> | T-PROD-SM-4-2 | No Hardcoded secrets exist in the production environment. | 5 | - | - | - |
> | T-PROD-SM-4-3 | Regular monitoring of public databases, systems, information channels, and other Internet (including dark-web) sources is performed to detect leaked company secrets. | 5 | - | - | - |
> </details>

> <details>
> <summary>Penetration testing in PROD environment [T-PROD-PENTEST]</summary>
>
> | ID | Practices | DAF maturity pyramid level | BSIMMv14 | DSOMM | SAMMv2 | 
> | --- | --- | --- | --- | --- | --- |
> | T-PROD-PENTEST-1-1 | Black-box penetration tests of the Prod environment are performed (the tester knows only basic information such as domain names and IP addresses). | 2 | - | - | - |
> | T-PROD-PENTEST-1-2 | Penetration testing is conducted regularly in the Prod environment. | 2 | PT1.1 | - | - |
> | T-PROD-PENTEST-1-3 | Gray-box penetration tests are performed (the tester knows the environment architecture and the analyzed software, including versions, and has access to the source code). | 2 | PT2.2 | - | - |
> | T-PROD-PENTEST-2-1 | A documented procedure detailing the methodology and the conditions under which penetration testing is performed in the Prod environment is defined and applied | 3 | - | - | - |
> | T-PROD-PENTEST-3-1 | A bug bounty program is established and operated. | 4 | CMVM3.4 | - | - |
> | T-PROD-PENTEST-4-1 | Social-engineering penetration tests targeted and adapted to developers are performed. | 7 | - | - | - |
> | T-PROD-PENTEST-4-2 | Red Team / Purple Team exercises are conducted with developer teams. | 7 | PT3.1, CMVM3.3 | - | EG-A-2 |
> </details>

> <details>
> <summary>Dynamic Application Security Testing (DAST) in PROD environment [T-PROD-DAST]</summary>
>
> | ID | Practices | DAF maturity pyramid level | BSIMMv14 | DSOMM | SAMMv2 | 
> | --- | --- | --- | --- | --- | --- |
> | T-PROD-DAST-1-1 | DAST scanning is used at least for the user interface. | 4 | - | 152 | - |
> | T-PROD-DAST-1-2 | Passive DAST scanning via traffic mirroring in PROD environment is used. | 4 | - | - | - |
> | T-PROD-DAST-1-3 | Dynamic scanning in PROD environment is performed manually. | 4 | - | - | - |
> | T-PROD-DAST-2-1 | Both active and passive DAST scanning mechanisms in PROD environment are used. | 5 | - | - | - |
> | T-PROD-DAST-2-2 | Unauthenticated DAST scanning in PROD environment is performed with full UI coverage, including:</br>- spider scanning (e.g., ZAP Spider);</br>- dependency scanning. | 5 | - | 122, 123 | - |
> | T-PROD-DAST-2-3 | Authenticated DAST scanning in PROD environment is performed, including:</br>- dependency scanning;</br>- exercising all available roles and user types;</br>- support for existing sessions;</br>- use of log-in/log-out flows;</br>- spider scanning after authentication. | 5 | - | - | - |
> | T-PROD-DAST-2-5 | Unused DAST scanner rules are disabled. | 5 | - | - | - |
> | T-PROD-DAST-3-1 | DAST scanning in PROD environment includes hidden paths. | 6 | - | 123 | - |
> | T-PROD-DAST-3-2 | Customized DAST scanner parameters in PROD environment are used to maximize input-parameter coverage and improve overall scan scope. | 6 | - | 124 | - |
> | T-PROD-DAST-3-3 | DAST scanning in PROD environment includes business-logic paths (e.g., logging in, updating account details, adding items to the cart). | 6 | - | 122 | - |
> | T-PROD-DAST-3-4 | Separate DAST scanning in PROD environment of backend and frontend is performed, including:</br>- scanning of SOAP services;</br>- scanning of proxy services relaying requests between frontend and backend;</br>- fuzzing of XML and JSON data sent to API services. | 6 | ST2.6 | - | - |
> | T-PROD-DAST-4-1 | DAST scanning in PROD environment covers all paths and interactions (including with the backend). | 7 | - | 123, 124 | - |
> | T-PROD-DAST-4-2 | Use of multiple DAST scanner engines in PROD environment increases coverage and enables cross-validation of results. | 7 | - | 137 | - |
> | T-PROD-DAST-4-3 | Custom dynamic-testing profiles with increased intensity and rigor are used for critical parts of the application in PROD environment. | 7 | - | 136 | - |
> </details>

> <details>
> <summary>Management of Infrastructure changes and access permissions [T-PROD-ACCESS]</summary>
>
> | ID | Practices | DAF maturity pyramid level | BSIMMv14 | DSOMM | SAMMv2 | 
> | --- | --- | --- | --- | --- | --- |
> | T-PROD-ACCESS-1-1 | IaC configuration for PROD environment is stored both within and outside the centralized source code repository (SCM). | 1 | - | - | - |
> | T-PROD-ACCESS-1-2 | The production environment is defined as code, is regularly updated, and is reproducible. | 1 | - | 86 | - |
> | T-PROD-ACCESS-1-3 | A version-control process for IaC configuration is implemented for PROD environment. | 1 | - | - | - |
> | T-PROD-ACCESS-1-4 | Access to the production environment is limited to a trusted set of users. | 1 | - | - | - |
> | T-PROD-ACCESS-1-5 | Use of default passwords in PROD environment is prohibited. | 1 | - | - | - |
> | T-PROD-ACCESS-2-1 | Access to infrastructure configuration code in PROD environment (IaC files) is limited to a small set of users. | 3 | - | - | - |
> | T-PROD-ACCESS-2-2 | Auditing of all changes to deployment configurations for any environment is configured, enabled, and processed. | 3 | - | 108, 106, 101 | - |
> | T-PROD-ACCESS-3-1 | Deployment to all non-production environments is automated. | 4 | - | - | - |
> | T-PROD-ACCESS-4-1 | Deployment to all production environments is automated. | 7 | - | - | - |
> </details>

> <details>
> <summary>Network traffic monitoring and control (L4–L7) [T-PROD-NETWORK]</summary>
>
> | ID | Practices | DAF maturity pyramid level | BSIMMv14 | DSOMM | SAMMv2 | 
> | --- | --- | --- | --- | --- | --- |
> | T-PROD-NETWORK-1-1 | Network traffic filtering at the firewall level (L3/L4) is in place in the PROD environment. | 1 | SE1.2 | - | - |
> | T-PROD-NETWORK-1-2 | The PROD infrastructure resides in a dedicated network segment. | 1 | - | 156 | - |
> | T-PROD-NETWORK-2-1 | Global network policies are configured and applied at the containerization layer. | 2 | - | 156 | - |
> | T-PROD-NETWORK-2-2 | L7 traffic-control policies are configured and applied. | 2 | SE1.1 | - | - |
> | T-PROD-NETWORK-3-1 | Customized network policies are configured and applied for individual microservices (namespaces). | 3 | - | - | - |
> </details>

> <details>
> <summary>Runtime environment monitoring and control [T-PROD-RUN]</summary>
>
> | ID | Practices | DAF maturity pyramid level | BSIMMv14 | DSOMM | SAMMv2 | 
> | --- | --- | --- | --- | --- | --- |
> | T-PROD-RUN-1-1 | Runtime controls for containerized environments (e.g., Kyverno, OPA Gatekeeper, Pod Security Admission, other validating tools) are used with default settings. | 2 | - | - | - |
> | T-PROD-RUN-2-1 | Customized runtime policies for containerized environments are used at least at the cluster-wide level. | 3 | - | - | - |
> | T-PROD-RUN-3-1 | Customized runtime policies are configured and applied for individual containerized applications. | 5 | SE3.3 | - | - |
> </details>

> <details>
> <summary>Vulnerability management (PROD Infrastructure) [T-PROD-VULN]</summary>
>
> | ID | Practices | DAF maturity pyramid level | BSIMMv14 | DSOMM | SAMMv2 | 
> | --- | --- | --- | --- | --- | --- |
> | T-PROD-VULN-1-1 | Infrastructure vulnerability scanning is performed manually and on an ad hoc basis. | 1 | - | - | - |
> | T-PROD-VULN-1-2 | Infrastructure components are regularly updated, including the remediation of identified vulnerabilities. | 1 | - | 9 | EM-B-2 |
> | T-PROD-VULN-2-1 | Regular vulnerability scanning is performed for PROD environment components exposed to the Internet, and remediation process is in place. | 2 | - | - | - |
> | T-PROD-VULN-2-2 | Regular asset-inventory tasks for PROD environment are performed using automation tools. | 2 | SM3.1, AM2.9, CMVM2.3 | - | - |
> | T-PROD-VULN-2-3 | Security updates are regularly installed on key PROD environment elements (e.g., the orchestrator and server operating systems). | 2 | - | - | EM-B-3 |
> | T-PROD-VULN-3-1 | Regular vulnerability scanning of all PROD infrastructure components is performed, and remediation process is in place. | 3 | CMVM3.5 | - | - |
> | T-PROD-VULN-3-2 | Automated checks of key PROD infrastructure components (e.g., the orchestrator and server operating systems) against security standards (based on best practices) are performed, with a process in place for correcting non-compliant settings. | 3 | CMVM3.5 | - | - |
> | T-PROD-VULN-3-3 | Regular vulnerability scanning of the PROD infrastructure is performed using automated tools in a penetration-test mode. | 3 | CMVM3.5 | - | - |
> | T-PROD-VULN-3-4 | Security updates are regularly installed on all PROD infrastructure elements (e.g., the orchestrator and server operating systems, web servers, database servers, etc). | 3 | - | - | - |
> | T-PROD-VULN-4-1 | Automated compliance checks of all PROD infrastructure components against security standards (based on best practices) are performed, with a process in place for correcting non-compliant settings. | 5 | CMVM3.5 | - | PC-A-3 |
> | T-PROD-VULN-4-2 | Outdated, vendor-unsupported software in the PROD infrastructure is regularly updated. | 5 | - | - | OM-B-3 |
> </details>

> <details>
> <summary>Security events monitoring and management [T-PROD-EVENTS]</summary>
>
> | ID | Practices | DAF maturity pyramid level | BSIMMv14 | DSOMM | SAMMv2 | 
> | --- | --- | --- | --- | --- | --- |
> | T-PROD-EVENTS-2-1 | An audit policy for the PROD infrastructure (e.g., a Kubernetes audit policy) is defined and applied. Logs are collected but not processed (e.g., retained within the Kubernetes cluster). | 2 | - | 108 | - |
> | T-PROD-EVENTS-3-1 | All PROD infrastructure logs (e.g., Kubernetes) are processed in the SIEM, with correlation rules configured to identify cybersecurity incidents. | 3 | SE3.3, CMVM1.1 | 106 | - |
> </details>


### Training and knowledge management

> <details>
> <summary>DevSecOps secure development training [P-EDU-AWR]</summary>
>
> | ID | Practices | DAF maturity pyramid level | BSIMMv14 | DSOMM | SAMMv2 | 
> | --- | --- | --- | --- | --- | --- |
> | P-EDU-AWR-1-1 | Basic cybersecurity training program is in place | 1 | - | 36 | EG-A-1 |
> | P-EDU-AWR-1-2 | Cybersecurity training for development teams is delivered on an ad hoc basis | 1 | - | 53 | - |
> | P-EDU-AWR-2-1 | Regular cybersecurity training is provided to all developers (external, internal, and e-learning). | 3 | T1.1, T2.9 | 36 | EG-A-2 |
> | P-EDU-AWR-2-2 | The developer training process is formalized (e.g., a cybersecurity awareness and secure-development training policy is in place). | 3 | - | 36 | EG-A-3 |
> | P-EDU-AWR-2-3 | Special cybersecurity training for Security Champions is conducted. | 3 | T2.5, T2.9 | 51 | EG-A-2 |
> | P-EDU-AWR-2-4 | A centralized platform for cybersecurity training is implemented and in use. | 3 | - | - | EG-A-3 |
> | P-EDU-AWR-3-1 | A program promoting internal knowledge sharing is implemented and operating. | 5 | T2.12 | 49 | EG-B-3 |
> | P-EDU-AWR-3-2 | An incentive system for completing cybersecurity training is developed and implemented. | 5 | T3.1 | - | - |
> | P-EDU-AWR-4-1 | The Information Security team regularly participates in CTF-style exercises or trainings in a cyber range in the context of web security and SSDLC | 6 | - | - | - |
> </details>

> <details>
> <summary>DevSecOps knowledge base management [P-EDU-KB]</summary>
>
> | ID | Practices | DAF maturity pyramid level | BSIMMv14 | DSOMM | SAMMv2 | 
> | --- | --- | --- | --- | --- | --- |
> | P-EDU-KB-1-1 | Team-level local knowledge databases are maintained within individual development teams. | 1 | - | - | - |
> | P-EDU-KB-2-1 | A centralized resource (common knowledge database) exists that stores basic rules and recommendations for secure development. | 3 | SM1.1, SR1.1, SR1.2 | - | - |
> | P-EDU-KB-2-3 | The unified knowledge database is updated irregularly; no formally assigned owners are in place, and no QA is performed. | 3 | SR1.1, SR1.2 | - | - |
> | P-EDU-KB-3-1 | The centralized resource stores unified, detailed rules and recommendations for secure development applicable to the company as a whole and to individual development teams. | 4 | SR1.2, SR3.3 | - | - |
> | P-EDU-KB-3-2 | The unified knowledge database is updated regularly; responsible owners are assigned at both team and company levels, and QA of the materials is performed. | 4 | SR1.2, SR2.2 | - | - |
> | P-EDU-KB-3-3 | The knowledge base is populated with real examples identified during penetration tests, bug bounty activities, and AppSec triage, including complex cases (e.g., business-logic issues). | 4 | - | - | - |
> | P-EDU-KB-4-1 | Documentation standards are developed and implemented; the unified knowledge database adheres to these standards and contains the required set of documents and information for the software under development. | 5 | - | - | - |
> | P-EDU-KB-4-2 | The knowledge database includes detailed cases with technical specifics and a CTF-like lab replica to support training. | 6 | - | - | - |
> </details>


### Software security requirements management

> <details>
> <summary>Software criticality assessment and threat modeling [P-REQ-TM]</summary>
>
> | ID | Practices | DAF maturity pyramid level | BSIMMv14 | DSOMM | SAMMv2 | 
> | --- | --- | --- | --- | --- | --- |
> | P-REQ-TM-1-1 | Threat modeling is performed to meet compliance requirements (e.g., for regulated systems) or for the most critical systems. | 2 | - | - | - |
> | P-REQ-TM-1-2 | Formal applicatio business criticality criterias are defined. | 2 | AA1.4 | - | TA-A-1 |
> | P-REQ-TM-1-3 | Business-criticality assessment is conducted for all newly developed applications. | 2 | AA1.4 | - | TA-A-1 |
> | P-REQ-TM-2-1 | Threat models are developed, including for infrastructure components. | 3 | - | 41 | - |
> | P-REQ-TM-2-2 | Threat modeling is performed for all new applications. | 3 | AA1.1 | - | - |
> | P-REQ-TM-2-3 | Business-criticality assessment is performed for all applications. | 3 | AA1.4 | - | TA-A-2 |
> | P-REQ-TM-3-1 | Threat models are developed for business processes as well. | 4 | - | 40 | SM-A-1 |
> | P-REQ-TM-3-2 | The threat-modeling process for developed software is standardized (templates are available; approaches for updating threats are defined). | 4 | AM1.3, AA2.1, AA2.2 | 30 | TA-B-2 |
> | P-REQ-TM-3-3 | Threat models are reviewed regularly. | 4 | - | 41 | TA-B-3 |
> | P-REQ-TM-4-1 | “Abuse cases” (illegitimate-use scenarios) are defined for each software product under development and are considered during threat modeling and subsequent changes. | 5 | AM2.1 | 28, 29 | RT-B-2  |
> </details>

> <details>
> <summary>Defining security requirements for applications under development [P-REQ-RD]</summary>
>
> | ID | Practices | DAF maturity pyramid level | BSIMMv14 | DSOMM | SAMMv2 | 
> | --- | --- | --- | --- | --- | --- |
> | P-REQ-RD-1-1 | Baseline security requirements for software under development are defined and applied. | 1 | - | - | SR-A-2  |
> | P-REQ-RD-1-2 | Information Security specialists review and approve decisions that affect the security posture of the application under development. | 1 | - | - | SR-A-2  |
> | P-REQ-RD-2-1 | Additional security requirements are defined based on threats identified through threat modeling. | 2 | - | - | - |
> | P-REQ-RD-2-2 | Security requirements are standardized (e.g., checklists are developed). | 2 | - | - | SR-A-2 |
> | P-REQ-RD-2-3 | Information Security specialists are involved in software architecture design | 2 | SFD1.2 | - | - |
> | P-REQ-RD-3-1 | Additional security requirements for business functions are defined based on the results of threat modeling. | 4 | - | - | TA-B-2 |
> | P-REQ-RD-3-2 | Additional security requirements are defined based on the results of risk analysis. | 4 | - | - | - |
> | P-REQ-RD-3-3 | The Architecture Committee makes key decisions that affect the security posture of applications under development | 4 | - | - | SA-A-3 (???) |
> | P-REQ-RD-4-1 | All features undergo review and approval by Information Security at the planning stage. | 6 | - | - | - |
> </details>

> <details>
> <summary>Verification of compliance with security requirements [P-REQ-CR]</summary>
>
> | ID | Practices | DAF maturity pyramid level | BSIMMv14 | DSOMM | SAMMv2 | 
> | --- | --- | --- | --- | --- | --- |
> | P-REQ-CR-1-1 | Security requirements for applications under development are verified at the release-to-production stage. | 1 | SM1.4, CP2.3 | 151 | SB-A-3 |
> | P-REQ-CR-2-1 | Adherence to security requirements for applications under development is verified through functional security testing and penetration testing. | 2 | SM1.4, CP2.3, ST1.3 | 148 | RT-B-2, ST-B-2 |
> | P-REQ-CR-3-1 | Application code is validated to confirm it is free of known vulnerabilities (e.g., via documented quality gates). | 5 | SM1.4, SM2.2 | - | SD-A-2, SB-A-3 |
> | P-REQ-CR-4-1 | The technical specification and architecture design are reviewed and approved with security requirements taken into account. | 6 | SM1.4 | - | AA-A-1 |
> </details>

> <details>
> <summary>Software security configuration standards for App [P-REQ-STDR-App]</summary>
>
> | ID | Practices | DAF maturity pyramid level | BSIMMv14 | DSOMM | SAMMv2 | 
> | --- | --- | --- | --- | --- | --- |
> | P-REQ-STDR-App-1-1 | Configuration standards for applications under development exist but are not formalized (i.e., recommendations or legacy settings rather than formal standards). | 3 | - | - | EM-A-1 |
> | P-REQ-STDR-App-1-2 | Configuration standards (recommendations, legacy settings) for applications under development are applied manually. | 3 | - | - | - |
> | P-REQ-STDR-App-2-1 | Configuration standards for applications under development  are defined for key systems. | 4 | - | - | EM-A-1 |
> | P-REQ-STDR-App-3-1 | Configuration standards are developed and applied for all systems. | 5 | - | - | EM-A-2 |
> | P-REQ-STDR-App-3-3 | Infrastructure-as-Code (IaC) approach is used to manage the configuration of an application | 5 | - | - | - |
> | P-REQ-STDR-App-4-1 | Configuration profiles are updated regularly using a risk-based approach. | 6 | - | - | EM-A-3 |
> </details>

> <details>
> <summary>Software security configuration standards for Infrastructure [P-REQ-STDR-Infr]</summary>
>
> | ID | Practices | DAF maturity pyramid level | BSIMMv14 | DSOMM | SAMMv2 | 
> | --- | --- | --- | --- | --- | --- |
> | P-REQ-STDR-Infr-1-1 | Infrastructure configuration standards are defined but not formalized (i.e., recommendations or legacy settings rather than standards). | 1 | - | - | - |
> | P-REQ-STDR-Infr-1-2 | Infrastructure configuration standards (recommendations, legacy settings) are applied manually. | 1 | - | - | - |
> | P-REQ-STDR-Infr-2-1 | Infrastructure configuration standards are developed for key infrastructure systems. | 2 | SR3.4 | - | - |
> | P-REQ-STDR-Infr-2-2 | Selective oversight of adherence to infrastructure configuration standards is performed without automation. | 2 | - | - | - |
> | P-REQ-STDR-Infr-3-1 | Infrastructure configuration standards are developed and applied for all systems. | 3 | SR3.4 | - | - |
> | P-REQ-STDR-Infr-3-2 | Automated tools are used to monitor/enforce adherence to infrastructure configuration standards. | 3 | - | - | - |
> | P-REQ-STDR-Infr-3-3 | Infrastructure-as-Code (IaC) approach is used to manage configuration of infrastructure components. | 3 | - | - | - |
> | P-REQ-STDR-Infr-4-1 | Infrastructure configuration standards are updated regularly using a risk-based approach. | 5 | - | - | - |
> </details>

### Security defects management

> <details>
> <summary>Security defects handling [P-DEFECT-MNG]</summary>
>
> | ID | Practices | DAF maturity pyramid level | BSIMMv14 | DSOMM | SAMMv2 | 
> | --- | --- | --- | --- | --- | --- |
> | P-DEFECT-MNG-1-1 | Handling of security defects in applications under development is performed as needed (ad hoc) and lacks a formal process | 1 | - | 135 | DM-A-2 |
> | P-DEFECT-MNG-2-1 | Critical-severity defects are remediated as a priority | 2 | - | 168 | DM-A-2 |
> | P-DEFECT-MNG-2-2 | Automated identification of security defects is part of the CI/CD process | 2 | SM3.4 | 185, 134 | SD-A-2 |
> | P-DEFECT-MNG-3-1 | For each information security defect, a task (ticket) is created in a task management system (e.g., Jira). The remediation of the defect (task completion) is monitored and tracked. | 3 | PT1.2, CMVM1.3, CMVM3.1 | - | DM-A-2 |
> | P-DEFECT-MNG-3-2 | An SLA for security defects remediation is implemented and enforced. | 3 | - | - | DM-A-3 |
> | P-DEFECT-MNG-3-3 | At the quality gate, verification is performed that no security defects above the defined severity threshold remain (this is a passing criteria). | 3 | SM2.2 | 167, 169 | SB-A-3 |
> | P-DEFECT-MNG-4-1 | Security defects are handled in accordance with a risk-based approach. | 7 | - | - | DM-A-2 |
> </details>

> <details>
> <summary>Security defects consolidation [P-DEFECT-CNS]</summary>
>
> | ID | Practices | DAF maturity pyramid level | BSIMMv14 | DSOMM | SAMMv2 | 
> | --- | --- | --- | --- | --- | --- |
> | P-DEFECT-CNS-1-1 | A centralized repository for security defect reports for applications in development is in place and actively used. | 3 | CR2.8 | 140 | - |
> | P-DEFECT-CNS-1-2 | Reporting is exported and centrally stored for a set of security checks/tools. | 3 | - | - | - |
> | P-DEFECT-CNS-2-1 | Reporting is exported and centrally stored for all security checks/tools used by the company to analyze applications in development. | 4 | CR2.8 | 140 | - |
> | P-DEFECT-CNS-3-1 | An SGRC platform is implemented and used for report management. | 5 | SM3.1 | - | - |
> | P-DEFECT-CNS-3-2 | Reports are uploaded to SGRC manually. | 5 | SM3.1, CR2.8 | - | - |
> | P-DEFECT-CNS-4-1 | Reports are uploaded to SGRC automatically. | 6 | SM3.1, CR2.8 | - | - |
> | P-DEFECT-CNS-4-2 | A roster of responsible owners for handling security defects is maintained, with defined escalation paths for remediation. | 6 | - | - | - |
> </details>


### DSO process effectiveness management

> <details>
> <summary>Security metrics management [P-MET-SET]</summary>
>
> | ID | Practices | DAF maturity pyramid level | BSIMMv14 | DSOMM | SAMMv2 | 
> | --- | --- | --- | --- | --- | --- |
> | P-MET-SET-2-1 | DSO process metrics are defined, documented, and tracked. | 3 | SM3.3 | - | SM-B-1 |
> | P-MET-SET-2-2 | Target values are defined for each DSO process metric. | 3 | - | - | SM-B-2 |
> | P-MET-SET-3-1 | Collected DSO process metrics are reviewed regularly. | 4 | SM3.3 | - | - |
> | P-MET-SET-3-2 | Target metric values are adjusted on a regular basis. | 4 | - | - | SM-B-3 |
> </details>

> <details>
> <summary>Security metrics compliance control [P-MET-EX]</summary>
>
> | ID | Practices | DAF maturity pyramid level | BSIMMv14 | DSOMM | SAMMv2 | 
> | --- | --- | --- | --- | --- | --- |
> | P-MET-EX-2-1 | DSO process metrics are collected and analyzed. | 3 | SM3.3 | - | - |
> | P-MET-EX-2-2 | Reports are generated and DSO metric results are compared with the target values. | 3 | - | - | - |
> | P-MET-EX-3-1 | Metrics are collected and analyzed for all teams. | 4 | - | - | - |
> | P-MET-EX-3-2 | The effectiveness of implemented measures is evaluated regularly based on DSO process metrics. | 4 | - | - | - |
> | P-MET-EX-3-3 | DSO metric results are visualized via dashboards (e.g., Grafana). | 4 | SM2.1 | - | - |
> | P-MET-EX-4-1 | Business process improvements are driven by DSO metrics; examples exist and/or the process is documented. | 6 | CP3.3 | - | - |
> </details>


### DSO process roles and responsibilities

> <details>
> <summary>Security Champions [P-ROLE-SC]</summary>
>
> | ID | Practices | DAF maturity pyramid level | BSIMMv14 | DSOMM | SAMMv2 | 
> | --- | --- | --- | --- | --- | --- |
> | P-ROLE-SC-1-1 | Security Champion functions are performed by Information Security specialists | 1 | - | - | - |
> | P-ROLE-SC-2-1 | A designated Security Champion is assigned to the team/project. | 3 | - | 50 | EG-B-1 |
> | P-ROLE-SC-2-2 | Security Champion promotes secure-development best practices within the team and shares vulnerability information and new security methods/practices with the AppSec team. | 3 | - | 43 | - |
> | P-ROLE-SC-3-1 | Security Champion conducts R&D on new security tools and reports results to the AppSec team. | 4 | - | - | - |
> | P-ROLE-SC-3-2 | Security Champion keeps secure-development tooling up to date. | 4 | CR1.7 | - | - |
> | P-ROLE-SC-3-3 | Security Champion performs code security reviews within their area of expertise. | 4 | - | - | EG-B-1  |
> | P-ROLE-SC-3-4 | Security Champion participates in PoC development and testing of new security tools. | 4 | - | - | - |
> | P-ROLE-SC-4-1 | Security Champion delivers secure-development and broader security training for new developers. | 7 | Т1.8 | - | - |
> | P-ROLE-SC-4-2 | Security Champion rotates into the AppSec team for up to three months as part of a staff-rotation program. | 7 | - | - | - |
> | P-ROLE-SC-4-3 | Security Champion reviews threat models and secure design, and conducts peer reviews of work performed by other Security Champions. | 7 | - | - | - |
> | P-ROLE-SC-4-4 | Security Champion develops PoCs for new exploits and verifies applications for compliance with security requirements. | 7 | - | - | - |
> </details>

> <details>
> <summary>DSO process roles segregation [P-ROLE-RESP]</summary>
>
> | ID | Practices | DAF maturity pyramid level | BSIMMv14 | DSOMM | SAMMv2 | 
> | --- | --- | --- | --- | --- | --- |
> | P-ROLE-RESP-1-1 | Information Security department has designated specialists responsible for the security of applications in development (in addition to their other duties). | 1 | - | - | EG-B-2 |
> | P-ROLE-RESP-1-2 | Responsibility for the security of applications in development is formally assigned (e.g., via policies, orders, or job descriptions). | 1 | - | - | - |
> | P-ROLE-RESP-2-1 | Dedicated Information Security roles accountable for application security during development are appointed. | 3 | - | - | - |
> | P-ROLE-RESP-2-2 | DSO roles matrix is defined. | 3 | - | - | - |
> | P-ROLE-RESP-2-3 | DevSecOps process  policy is developed and in effect. | 3 | - | - | PC-A-1 |
> | P-ROLE-RESP-2-4 | DevSecOps process  roadmap exists and is approved. | 3 | - | - | SM-A-2 |
> | P-ROLE-RESP-3-1 | A RACI matrix for the end-to-end DSO process is developed, approved and in use. | 4 | - | - | - |
> | P-ROLE-RESP-3-2 | DevSecOps process  roadmap is regularly reviewed and updated to reflect business objectives and external factors. | 4 | - | - | SM-A-3 |
> </details>

