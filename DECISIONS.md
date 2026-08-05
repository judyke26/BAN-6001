# Decision Log

## Assignment 2: Dataset  (2026-07-19)
- Dataset: College Scorecard, Most Recent Cohorts: Institution-Level Data
 from U.S. Department of Education. (2026). College Scorecard: Most recent cohorts, institution-level data [Data set]. https://collegescorecard.ed.gov/data
- Main variable of interest: median_earnings_10yr
 because we would like to see how college decisions affect the earnings of students post-grad. 
- Key decision: We chose this dataset over alternatives because it combines financial, demographic, and outcome variables for nearly 1,400 institutions in one place. This dataset gave enough variation (public vs. private, selective vs. open-admission, different regions) to support meaningful comparisons in later assignments.

## Assignment 3: Descriptive Stats  (2026-07-26)
- Cleaning done: The original data contained 3,308 variables and 6,273 schools in total. We eliminated and all but the 13 most essential variables while recoding 4 others to contain 3 or less categories(control_type, locale_type, region, and high_earnings). Additionally, we renamed all the variables, making them easier to understand at a glance. All of the final 17 will play a part in our central focus of median earnings after 10 years. We then filtered the schools to only 4-year institutions that predominantly award bachelor's degrees, due to two-year and certificate programs under-reporting admission, retention, and completion rates (missing values). This removed 4,866 entries and we were left with a final total of 1,407 schools.
- Most surprising pattern: Most surprising pattern: School size (undergrad enrollment) was heavily right-skewed — the median was only 2,135 students, but the max reached 163,164. Several other continuous variables showed similar skew. Categorical variables were more evenly distributed, though Private For-Profit schools were notably underrepresented (2.2%) versus Private Nonprofit (62%), and the West region had far fewer schools (18.8%) than the East (44.2%). We also noticed what looks like a vertical asymptote in the median earnings vs. median grad debt scatterplot, which we don't fully understand yet.

## Assignment 4: Probability  (2026-07-26)
- Normal vs. empirical, and why: We checked normality across several continuous variables. completion_rate came closest to a normal distribution (skewness ≈0.10, kurtosis ≈-0.07), with normal-model quartiles (0.463, 0.701) nearly matching the actual data quartiles (0.469, 0.700), so we treated it as approximately normal for probability estimates. Most other variables — admission_rate, undergrad_enrollment, tuition_out_of_state, median_grad_debt, median_earnings_10yr, avg_faculty_salary, and student_faculty_ratio — were meaningfully skewed, several right-skewed due to a small number of large research universities and expensive private schools, so we relied on empirical distributions for those instead of assuming normality.

## Assignment 5: Inference  (2026-08-09)
- What we tested, alpha, conclusion: 
Test 1: Out-of-state-tuition 
One-sample right-tailed t-test of H₀: μ ≤ $32,000 vs. Hₐ: μ > $32,000, α = 0.05. Sample mean = $34,294.57 (n = 1,407), t = 5.58, p ≈ 1.48×10⁻⁸. Since p < α, we reject H₀ — there's sufficient evidence average out-of-state tuition exceeds $32,000.
Test 2: 10-year median earnings
One-sample two-tailed t-test of H₀: μ = $55,000 vs. Hₐ: μ ≠ $55,000, α = 0.05. Sample mean = $58,036.25 (n = 1,407), t = 7.47, p ≈ 1.37×10⁻¹³. Since p < α, we reject H₀ — there's sufficient evidence the average differs from (and is higher than) $55,000.
We did a 95% confidence interval for 10-year median earnings. This was consistent with rejecting the $55,000 hypothesis.

## Assignment 6: Regression  (2026-08-12)
- First predictor removed and why: retention_rate was removed first because it had the highest p-value (0.789851), making it the most insignificant of the variables.
- Multicollinearity handling: ____
