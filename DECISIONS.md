# Decision Log

## Assignment 2: Dataset  (202X-YY-ZZ)
- Dataset: College Scorecard, Most Recent Cohorts: Institution-Level Data
 from U.S. Department of Education. (2026). College Scorecard: Most recent cohorts, institution-level data [Data set]. https://collegescorecard.ed.gov/data
- Main variable of interest: median_earnings_10yr
 because we would like to see how college decisions affect the earnings of students post-grad. 
- Key decision: We chose this dataset over alternatives because it combines financial, demographic, and outcome variables for nearly 1,400 institutions in one place. This dataset gave enough variation (public vs. private, selective vs. open-admission, different regions) to support meaningful comparisons in later assignments.

## Assignment 3: Descriptive Stats  (202X-YY-ZZ)
- Cleaning done: The original data contained 3,308 variables and 6,273 schools in total. We eliminated and all but the 13 most essential variables while recoding 4 others to contain 3 or less categories(control_type, locale_type, region, and high_earnings). Additionally, we renamed all the variables, making them easier to understand at a glance. All of the final 17 will play a part in our central focus of median earnings after 10 years. We then filtered the schools to only 4-year institutions that predominantly award bachelor's degrees, due to two-year and certificate programs under-reporting admission, retention, and completion rates (missing values). This removed 4,866 entries and we were left with a final total of 1,407 schools.
- Most surprising pattern: Most surprising pattern: School size (undergrad enrollment) was heavily right-skewed — the median was only 2,135 students, but the max reached 163,164. Several other continuous variables showed similar skew. Categorical variables were more evenly distributed, though Private For-Profit schools were notably underrepresented (2.2%) versus Private Nonprofit (62%), and the West region had far fewer schools (18.8%) than the East (44.2%). We also noticed what looks like a vertical asymptote in the median earnings vs. median grad debt scatterplot, which we don't fully understand yet.

## Assignment 4: Probability  (202X-YY-ZZ)
- Normal vs. empirical, and why: We checked normality across several continuous variables. completion_rate came closest to a normal distribution (skewness ≈0.10, kurtosis ≈-0.07), with normal-model quartiles (0.463, 0.701) nearly matching the actual data quartiles (0.469, 0.700), so we treated it as approximately normal for probability estimates. Most other variables — admission_rate, undergrad_enrollment, tuition_out_of_state, median_grad_debt, median_earnings_10yr, avg_faculty_salary, and student_faculty_ratio — were meaningfully skewed, several right-skewed due to a small number of large research universities and expensive private schools, so we relied on empirical distributions for those instead of assuming normality.

## Assignment 5: Inference  (202X-YY-ZZ)
- What we tested, alpha, conclusion: ____

## Assignment 6: Regression  (202X-YY-ZZ)
- First predictor removed and why: ____
- Multicollinearity handling: ____
