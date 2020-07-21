# Africa-DSI-Quiz. 
Here are my solutions, python codes I wrote to answer some of the questions in the Round 2 of the Quiz. Unfortunately, I couldn't save the questions before the quiz submission link closed. For the solutions involving code, the Jupyter Notebook files will better explain what my solutions were. All questions were multiple choice.

Q1. Given the list of integers, X, https://www.google.com/url?q=https://docs.google.com/document/d/1TjeNYpZ_PbdBISlJPF-_WqULBc1WpuYthLClovjB3Rs/edit?usp%3Dsharing&sa=D&ust=1594968749928000&usg=AFQjCNG8bAv1lX8pXr4CYcgaDfYFxcbgCg. 
Write code to count how many integers are strictly larger than all the integers to their right excluding the last digit since it doesn’t have a number to its right. E.g. for [2,3,1] the answer should be 1 while for [12,4,4,2,2,3] the answer is 2.  

If link is broken use X in Q1.ipynb file 


Q2. This was a brain teaser question available here and brainly https://brainly.in/question/19781664


Q3. Consider the binomial model, where the variable X is the total number of failures from a set of N produced electronic components. Let p be the probability of a failure and x the number of failures during a one year observation period. What is the standard deviation of the maximum likelihood estimator given that there were 37 failures observed out of a group of 840 electronic components during the one year observation period? 

I chose standard deviation (std) value of 0.00114 as answer because the likelihood funtion at this std value was had the maximum value.  (Check Q3.ipynb for how I got my solution)


Q4. This question had to do with 13 robbers who stole gold bars and had to share it equally amongst themselves. It turned out to have 3 left. One of the robbers attempted to fight and was thrown out by the leader of the gang. His/Her gold bars were taken and shared among the remaining 12. After each as received equally, 5 was left. Another attempted to fight and was thrown out by the leader of the gang. His/Her gold bars were taken and shared among the remaining 11. After each as received equally, 0 gold bars was left. The question asked to find out how many gold bars the robbers had if the gold bars were less than 750 (not so sure of the exact figure).

I obtained the answer (i.e. 341) using modulus. Check Q4.ipynb for my solution.


Q5. Robyn decides to organize a hiking trip and invites her friends - Dylan, Linda and Dominic to join her. On the days leading to the hike, her three friends say the following:Two Days Before the hike:Dylan: Dominic is going to the hike. Dominic: Linda is not going to the hike.Linda: Dylan will go to the hike if, and only if, I do.The Day Before the hike:Dylan: Linda will go to the hike if, and only if, I don't go. Dominic: An even number out of the three of us are going to the hike.Linda: Dylan is going to the hike.The Day of the hike:Dylan: It is not yet 2020. Dominic: Dylan will go to the hike if, and only if, I do.Linda: At least one of the three of us is not going to the hike. Robyn also knows that out of Dylan, Dominic, and Linda:One of them never lies.One lies on days of the month that are divisible by 2, but is otherwise truthful.The remaining one lies on days of the month that are divisible by 3, but is otherwise truthful.Can you figure out who is going to attend? 

I wasn't too confident of my answer for this question which was "Dominic and Dylan", so I choose my answer (Lynda and Dylan) by heart.


Q6. A No Claims Discount system is operated by a car insurer. There are four levels of discount: 0%, 10%, 25% and 40%. After a claim-free year a policy holder moves up one level (or remains at the 40% level if they are already there). If a policy holder makes one claim in a year he or she moves down one level (or remains at the 0% level if already there). A policyholder who makes more than one claim in a year moves down two levels (or moves to or remains at the 0% level). Changes in level can only happen at the end of each year. The probability of a claim in any given month is assumed to be constant at 0.04 (i.e. 4%). At most one claim can be made per month and claims are assumed independent. Calculate the proportion of policyholders in the long run who are at the 25% level. 

While attempting to obtained an answer, I got figures that were all but 0.2447. I knew the figures I obtained corresponding to P(making one claim in one year) = 12C1 * (0.04)**1 * (0.96)**11 = 0.3064, P(not making a claim in a year) = (0.96)**12 = 0.613 P(making any claim in a year) = 1 - 0.613 = 0.387. I knew none of these were the answers so I chose the number I didn't see in my workings, i.e 0.2447. The full solution can be found here https://www.assignmentexpert.com/homework-answers/mathematics/statistics-and-probability/question-126844


Q7. Suppose John writes down a single number that is in the range from 1 to 20, and Susan also writes down a single number from 1 to 20. What is the probability that John's pick would be a number greater than Susan's pick.

I wrote down a table with headers at the top and extreme left as 1, 2, 3 ... up to 20. and tried to match them in a 2-pair coordinate using their headings. So that it looks like (1,1) (1,2) (1,3) ... (1,20) for first row. And (2,1) (2,2) (2,3) ... (2, 20) for second row. Third row has (3,1) (3,2) (3,3) ... (3,20) and so forth up to the 20th row were we have (20,1) (20,2) (20,3) ... (20,20). It was like a 20x20 matrix with the pairs distributed in each cell of the matrix. I took the top headings as John's picks and left headings and  left headings as Susan's picks.
    1     2     3    4      5   6   7   8   9   10   11    12    13    14    15    16    17    18    19    20
1 (1,1) (1,2) (1,3) (1,4) (1,5) ...
2 (2,1) (2,2) (2,3) (2,4) (2,5) ...
...
18 (18,1) (18,2) (18,3) (18,4) ...
19 (19,1) (19,2) (19,3) (19,4) ...
20 (20,1) (20,2) (20,3) (20,4) ...
Now, pick all (x,y) pairs that have y greater than x such as (1,2), (2,3), (3,4),... on and on. The number of such pair will be 
19 for row 1,  18 for row 2, 17 for row 3, 16 for row 4 and so forth in that order. By row 20, you have nothing because (20,20) or (20, a) where is between 1 and 20 doesn't qualify because if Susan picks 20, there is no number John can pick that would be greater than Susan's. So the total number of valid pairs is 19 + 18 + 17 + 16 + ... + 2 + 1. This can be summed using n(n + 1)/2 where n is 19. The sum is 190. The total number of possibilities is 20 rows x 20 columns = 400. 
So probability = 190 / 400 = 0.475


Q8. This was another brain teaser on two heterosexual couples who make out at a party. One is an Engineer, one a mathematician, one a data scientist, one a lecturer. The couples are Indian and Chinese. The Chinese woman is a lecturer and her husband is a mathematician. The Engineer is a Chinese man. Mr. Patel is an Indian. What is Mrs. Patel's occupation? 

The answer was lecturer.


Q9. Q9 had to do with cards, ...can't really remember the question. 

The answer I chose was Card 1: Jack, Card 2: Queen, Card 3: King


Q10. An accounting company buys its computers from three different companies. 
Company X supplies 25% of the computers, company Y supplies 35% of the computers and company Z supplies the rest.
From past experience you determine that 5% of company X’s computers produced are defective, 4% of company Y’s computers are defective and 2% of company Z’s computers are defective.
If one of the computers were reported by one of the employees as defective, what is the probability that the computer was supplied by Company X?

( I solved this using Joint and Conditional Probability. Answer: 0.3623)


Q11. What text is encoded in the image? (Hint: load the image, look at the pixel values and think creatively). Image is Cat_Image.png in folder.

I could solve this. So I used my intuition and picked 'I lovve Kittens' because that was the odd one. The other options were names of AI researchers.


Q12. A dataset of training and test data (i.e. "heart_training_data.csv", "heart_test_data.csv") contains demographic and medical data of a set of patients. There are multiple features which include ID: is a unique identifier for each patient. sex:: the patient's gender, age: the patient's age and a number of other categorical and numerical variables, some of which will need to be cleaned. Use the training data to create a model using logistic regression that will predict whether a patient has a disease (target=1) or not (target=0). Applying the model to the test set, which of the following is closest to your answer?

Answer I obtained was (ID: 946 target:1, ID: 637 target:1, ID: 688 target:1, ID: 831 target:1). Check my solution in HeartData.ipynb


Q13. Using regex, pandas or whichever text cleaning techniques you like (though doing it by hand is not recommended!), find the 6th digit of the sum of all the rows and columns of numeric data in the file “Worldometers_data.csv” linked: (https://drive.google.com/drive/folders/1iQ9BnMNQj_CVvGbZLiDG7lyr3bSmproN?usp=sharing).
Replace any NaNs with 0 and strip any non-numeric characters. E.g. ‘1,23%4’ should become 1234. The sum is 16570X80.27. What is the digit X?

The answer is 3, check DataClean.ipynb for solution.


Q14. What is the area of the shaded region? You only know the length indicated. There is a solution (image is Q14.png). 

I solved this using intuition based on observation and ruler measurements. 
I observed that the radius of the circle quadrant was 15 andd that of the inner circle was 4.5. Area is (pi(15)**2)/4 - pi(4.5)**2. I obtained 36pi 
