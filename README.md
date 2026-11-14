# CS3SY26_ProjectProposal by FILLAR DIOKO NAZARREA

## Project Proposal Template

### Project Title or Name of the Application	: Probability Puzzles
### Section			   	      : Magnesium
### Group Members			    : DIOKO, FILLAR, NAZARREA
### Date (Proposal Date)  : November 10, 2026

### Project Description:

- A brief summary of the project description and the need for it.

- The project demonstrates counterintuitive concepts in Statistics and Probability. Scenarios where the first thing that comes to your mind is not the measured or correct outcome. It demonstrates that critical thinking is important in scenario analysis, and teaches students how to analyze scenarios carefully.

- We hope for this program to reach future statisticians, or anyone curious in improving their statistics skills and being facinated at how intuitive analysis may not always be correct. 

- The project shows scenarios such as the Monty Hall Paradox, the Birthday Paradox, Bertrand's Box Paradox, Boy or Girl Paradox, and the False Positive Paradox

## Class Descriptions

The following classes define the structure and functionality of the program.

### 1. `Paradox` (Abstract Class)

Serves as the parent class for all probability paradoxes, establishing their common attributes and methods.

**Attributes:**
- `name: str`
- `description: str`
- `theoretical_probability: float`

**Methods:**
- `simulate(): Result`
- `calculate_probability(): float`
- `explain_result(): str`

### 2. `MontyHall`

Simulates the Monty Hall problem, demonstrating how switching choices affects the probability of winning.

**Attributes:**
- `number_of_doors: int`
- `initial_choice: int`
- `host_revealed_door: int`
- `switched_choice: bool`

**Methods:**
- `simulate(): Result`
- `calculate_probability(): float`
- `explain_result(): str`

### 3. `BirthdayParadox`

Demonstrates how the probability of two or more people sharing a birthday increases with group size.

**Attributes:**
- `group_size: int`
- `days_in_year: int`

**Methods:**
- `simulate(): Result`
- `calculate_probability(): float`
- `explain_result(): str`

### 4. `BertrandsBox`

Simulates Bertrand's Box Paradox, demonstrating conditional probability through the selection of coins from different boxes.

**Attributes:**
- `box_selection: int`
- `coin_selection: int`

**Methods:**
- `simulate(): Result`
- `calculate_probability(): float`
- `explain_result(): str`

### 5. `BoyOrGirl`

Demonstrates how additional information about a family's children affects conditional probability.

**Attributes:**
- `family_information: str`
- `number_of_children: int`

**Methods:**
- `simulate(): Result`
- `calculate_probability(): float`
- `explain_result(): str`

### 6. `FalsePositive`

Demonstrates how test accuracy and prevalence influence the probability that a positive test result is correct.

**Attributes:**
- `prevalence_rate: float`
- `sensitivity: float`
- `specificity: float`

**Methods:**
- `simulate(): Result`
- `calculate_probability(): float`
- `explain_result(): str`

### 7. `ParadoxManager`

Manages the collection of available paradoxes and allows the program to retrieve specific scenarios.

**Attributes:**
- `paradoxes: List[Paradox]`

**Methods:**
- `add_paradox(paradox: Paradox): void`
- `remove_paradox(name: str): void`
- `get_paradox(name: str): Paradox`
- `get_all_paradoxes(): List[Paradox]`

### 8. `Simulation`

Handles the execution of a selected paradox and manages the number of simulation trials.

**Attributes:**
- `number_of_trials: int`
- `completed_trials: int`

**Methods:**
- `run(paradox: Paradox): Result`
- `reset(): void`

### 9. `Result`

Stores the theoretical and experimental outcomes of a simulation.

**Attributes:**
- `theoretical_probability: float`
- `experimental_probability: float`
- `total_trials: int`
- `explanation: str`

**Methods:**
- `calculate_difference(): float`
- `display_result(): void`

---

## Class Relationships

The classes interact through the following relationships:

| Relationship | Classes Involved | Description |
|---|---|---|
| **Inheritance** | `Paradox` → Individual Paradox Classes | Each individual paradox inherits common attributes and methods from the abstract `Paradox` class. |
| **Aggregation** | `ParadoxManager` → `Paradox` | The manager maintains a collection of paradox objects. |
| **Association** | `Simulation` → `Paradox` | A simulation interacts with the selected paradox. |
| **Dependency** | `Simulation` → `Result` | A simulation generates a result after execution. |
| **Association** | `Result` → `Paradox` | Each result corresponds to the paradox being simulated. |

---

## UML Class Diagram

The following diagram illustrates the proposed class structure, including the attributes, methods, and relationships described above.

*The diagram represents the proposed architecture and may be modified during implementation.*

<img width="775" height="452" alt="Screenshot 2026-11-14 at 8 48 13 PM" src="https://github.com/user-attachments/assets/2e94ddee-b393-434d-b9d5-b7c56020b3e1" />

### Goals:

We hope for this project to improve people's understanding of Statistics and Probability by showing how intuitive analysis may not always lead to the correct outcome. Through different probability paradoxes and simulations, we aim to encourage critical thinking, careful scenario analysis, and curiosity about mathematical concepts. Ultimately, we hope to make learning Statistics and Probability more engaging and accessible to students and anyone interested in the subject.

Objectives

Objective 1: Develop a program that demonstrates different probability paradoxes through simulations, allowing users to observe and compare theoretical and experimental outcomes.

Objective 2: Encourage users to think critically and analyze scenarios carefully by understanding why their initial assumptions may differ from the actual mathematical outcomes.
