## Predictive Maintenance - Turbofan Engine RUL Prediction

I'm a final year STIC engineering student at INP-HB in Yamoussoukro, Côte d'Ivoire, and I finish in 5 months. I'm looking for a 6-month end-of-studies internship starting in March 2027, ideally at Air Côte d'Ivoire or ASECNA in Abidjan. I started this project to show what I can actually do with data instead of just talking about it in a CV.

## Dataset

I'm using the NASA C-MAPSS dataset (FD001 subset). It simulates 100 turbofan engines running until they fail, with 21 sensors recording values at every cycle. I don't have access to real airline maintenance data, so this public dataset is the closest thing I found to practice on before an internship. It's simulated, so I'm not claiming anything about real aircraft.

## What I'm doing

Basically I'm trying to predict the Remaining Useful Life (RUL) of an engine, meaning how many cycles are left before it breaks down. Given the sensor readings at a certain cycle, the model should guess how many cycles are left. Right now I'm treating it as a simple regression problem.

The idea I want to build around it: the model never decides alone. It proposes a RUL, a few simple safety rules can override it, and a human engineer always has the final word. I haven't built the rules part yet, it's in the roadmap below.

## Tech I use

I code in Python, with pandas and numpy to clean and explore the data. For the models I'm using scikit-learn, I started with Linear Regression and Random Forest as baselines, and now I'm trying XGBoost to see if it actually does better. I'm still learning ML properly so some of the code here is more "student trying things" than clean production code, but I'm improving it little by little.

## Roadmap for the next 4 months

I already loaded and explored the dataset and built a first baseline model with Linear Regression. Next I want to work on better feature engineering, things like rolling averages and picking which sensors are actually useful since some of them barely move. I'm also still testing XGBoost, the RMSE is not great yet so I need to keep working on it. After that I'd like to add a notebook with clear plots showing how the engines degrade over time, build the rules and human validation part, and make a small Streamlit demo. If I have time I'll try the other FD00x subsets too and write a short report with what worked and what didn't.

## Contact

Cheick Ousmane Diallo, final year engineering student at INP-HB Yamoussoukro.

- LinkedIn: https://www.linkedin.com/in/cheick-ousmane-diallo-95b537419/
- Email: cheick.diallo23@inphb.ci / diallo240500@gmail.com

Based in Yamoussoukro / Abidjan, open to an internship from March 2027.
