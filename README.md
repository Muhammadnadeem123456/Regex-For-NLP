Regular Expression in NLP:
chat1='here you ask a lot questions 1234567890, abc@xyz.com'
chat2='here it is (123)-567-8912, abc@xyz.com'
chat3='yes, phone:1234567890 email: abc@xyz.com'
1-MATCH WRITTEN CONTINUOUS DIGITS WRITTEN. \d{10}.
2-CONCATENATE BOTH FORMAT 1234567890 AND (123)-234-2432
e.g.; patter=r'\d{10}|\(\d{3}\)-\d{3}-\d{4}'
3-MATCHING EMAIL FORMAT
e.g.; [a-z0-9A-Z]*@[a-z]*\.com
for all patterns: [a-z0-9A-Z]*@[a-z]*\.[a-zA-Z]* 
like io, tech, , net etc
chatt1='I have issue with order#123421243'
chatt2='I have a problem with my order number123421243'
chatt3='my order 123421243 having issue'
1-order[^\d]*(\d*)

text='''
Born Elon Reeve Musk
June 28, 1971 (age 50)
Pretoria, Transvaal, South Africa
Citizenship	
South Africa (1971–present)
Canada (1971–present)
United States (2002–present)
Education	University of Pennsylvania (BS, BA)
Title	
Founder, CEO and Chief Engineer of SpaceX
CEO and product architect of Tesla, Inc.
Founder of The Boring Company and X.com (now part of PayPal)
Co-founder of Neuralink, OpenAI, and Zip2
Spouse(s)	
Justine Wilson

(m. 2000; div. 2008)
Talulah Riley

(m. 2010; div. 2012)

(m. 2013; div. 2016)
'''
1-RETRIEVING AGE
age (\d+)
2-RETRIEVING NAME
Born(.*)
3-RETRIEVING DATE OF BIRTH
Born.*\n(.*)\(age
4-Birth place 
\(age.*\n(.*)
