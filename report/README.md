# AAE6102 Laboratory Report

### Report Menu
1. [Parameter Tuning and Effects](#1-parameter-tuning-and-effects)
2. [Strengths and Limitations](#2-strengths-and-limitations)
3. [Kaggle Competition](#3-kaggle-competition)
4. [Comparison with Other Libraries (Optional)](#4-comparison-with-other-libraries-optional)
5. [Suggestions for Improvement](#5-suggestions-for-improvement)


## 1. Parameter Tuning and Effects
- List the parameters tuned.
- Explain how parameter changes affected:
    - **Accuracy**
    - **Processing speed**
    - **Robustness**

## 2. Strengths and Limitations
- **Strengths**: Flexibility, robustness, ease of use.
- **Limitations**: Computational efficiency, lack of specific features.

## 3. Kaggle Competition
Submit your positioning result and beat your classmate at [Kaggle competition](https://www.kaggle.com/competitions/aae-6102-laboratory/).

## 4. Comparison with Other Libraries (Optional)
If time permits, test another GNSS library using the same dataset and compare based on:
- **Accuracy**
- **Ease of use**
- **Flexibility**
- **Computational efficiency**

## 5. Suggestions for Improvement

### Recommandations for our used library:
**RTKLIB (tested on Ubuntu & Windows):**
- **Cross-Platform Consistency**: 

    RTKLIB operates on both Ubuntu and Windows, but inconsistencies in path formatting and file system handling can affect usability. Standardizing these behaviors would ensure a smoother cross-platform experience.
- **Lack of GUI on Ubuntu**: 

    Unlike the Windows version (which includes RTKNAVI, RTKPOST, etc.), the Ubuntu version lacks any graphical interface. Introducing a cross-platform GUI or web-based frontend would greatly improve usability, especially for configuration and debugging.
- **Multipath Mitigation**: 

    RTKLIB could be significantly improved by integrating modern multipath rejection and NLOS (Non-Line-of-Sight) detection techniques to boost positioning performance in urban and obstructed environments.
- **Codebase Modernization**: 

    Transitioning from C to a more modular C++ design with object-oriented principles would enhance maintainability and scalability.

**GraphGNSSLib (Docker-based):**

- **Docker Optimization**: 

    While the Docker setup is functional, it is not robust across different environments, often causing installation issues. Additionally, many users reported failures when starting the Docker container. Streamlining the Docker image and improving setup scripts would enhance reliability.
- **No GUI Support**: 

    GraphGNSSLib lacks a graphical interface under Ubuntu, making parameter tuning and debugging less intuitive. A lightweight Qt or web-based GUI for configuration would be highly beneficial, especially for beginners.
- **ROS Compatibility Limitation**: 

    GraphGNSSLib currently does not support ROS Noetic or later versions due to the missing `novatel_msgs` package. Updating dependencies or removing the reliance on deprecated packages is necessary for future ROS compatibility.
- **Scalability**: 

    Introducing multi-threaded computation and GPU-accelerated backends could help handle large datasets and improve performance in real-time applications.
- **Documentation and Examples**: 

    Expanding the documentation with practical examples, setup guides, and detailed parameter explanations would significantly lower the learning curve and promote adoption.

### Refining Parameter Tuning Process

- **Automated Search Tools**: Integrate support for automated hyperparameter optimization using methods like grid search or Bayesian optimization to streamline the tuning process.
- **Performance Evaluation Scripts**: Provide standardized tools to evaluate configurations based on metrics such as RMSE, fix ratio, convergence time, and computation time.
- **Environment-Specific Presets**: Include pre-configured parameter sets for common scenarios (e.g., open-sky, suburban, urban canyon) to help users quickly adapt to different conditions.
- **Visualization Support**: Add visualization utilities to analyze trajectory results, residuals, satellite geometry, and measurement quality, aiding in comprehensive evaluation.
- **Logging and Reproducibility**: Ensure all configuration files, parameter sets, and outputs are properly logged and version-controlled to support reproducibility and debugging.
