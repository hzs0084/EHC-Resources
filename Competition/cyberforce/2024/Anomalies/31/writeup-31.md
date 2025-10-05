Using body column: Body
Using subject column: Subject
Using from/sender column: From

--- RESULTS ---

Total stopwords removed (Answer1): 3515
Total tokens after tokenization (Answer2): 5596

Flag (ANOMALY PART 1) format -> Answer1;Answer2
3515;5596

Top 3 trigrams (ANOMALY PART 2):
1. 'please click link'  (count: 20)
2. 'details using link'  (count: 18)
3. 'please follow link'  (count: 17)

Flag (ANOMALY PART 2) format -> trigram1;trigram2;trigram3
please click link;details using link;please follow link

Most common subject line (ANOMALY PART 3):
Issue Detected with Your Recent Online Purchase
Most frequent sender domain (ANOMALY PART 3):
alphatechsolutions.com

Flag (ANOMALY PART 3) format -> most common subject line;mostfrequent.domain
Issue Detected with Your Recent Online Purchase;alphatechsolutions.com

Top 10 trigrams with counts (for debugging):
    20  please click link
    18  details using link
    17  please follow link
    16  click link participate
    14  please contact us
    14  contact us immediately
    14  us immediately best
    14  immediately best regards
    13  failure may result
    12  prompt attention matter
