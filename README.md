# Safety-Validation-Network

Overview

This project demonstrates a critical component of the Autonomous Vehicle (AV) development lifecycle: Automated Scenario Testing and Safety Validation.

It provides a lightweight Python framework to load recorded performance metrics (e.g., from simulation or test track runs) and systematically check them against pre-defined, safety-critical Acceptance Criteria. This process ensures that new software builds maintain required levels of safety and comfort before deployment, a core responsibility of a Technical Program Manager (TPM).

Key Functionality

Scenario Definition: Defines the parameters and safety requirements for a specific high-risk event (e.g., "Pedestrian J-Walk").

Dataset Processing: Simulates loading a large dataset of test results (Min Distance, Peak Deceleration).

Automated Compliance Check: Iterates through each test run and determines the outcome based on two criteria:

Critical Safety Check: Did the vehicle collide (Min Distance $\leq 0.0 \text{ ft}$)? (Result: FAIL)

Comfort/Soft Safety Check: Did the vehicle brake too hard (Deceleration $> 0.7\text{g}$)? (Result: PASS_WITH_WARNING)

Reporting: Generates a structured summary report, clearly quantifying the total PASS, PASS (Warning), and FAIL rates for the tested scenario, providing immediate, actionable data for release managers and engineering teams.

Technical Relevance to AV:

This tool showcases programmatic experience with:

Safety-critical system metrics.

Automating compliance checks (Test Infrastructure).

Bridging the gap between engineering test results and Go/No-Go release decisions (TPM accountability).
