```python
import nltk
import re 
```


```python
# nltk tool kit for natural language processing 
import nltk
nltk.download('punkt')
import nltk
nltk.download('maxent_ne_chunker')
nltk.download('words')
nltk.download('punkt')
```

    [nltk_data] Downloading package punkt to /home/kudsit/nltk_data...
    [nltk_data]   Package punkt is already up-to-date!
    [nltk_data] Downloading package maxent_ne_chunker to
    [nltk_data]     /home/kudsit/nltk_data...
    [nltk_data]   Package maxent_ne_chunker is already up-to-date!
    [nltk_data] Downloading package words to /home/kudsit/nltk_data...
    [nltk_data]   Package words is already up-to-date!
    [nltk_data] Downloading package punkt to /home/kudsit/nltk_data...
    [nltk_data]   Package punkt is already up-to-date!





    True




```python
### nltk tokenizations 

import nltk
nltk.download('punkt_tab')

```

    [nltk_data] Downloading package punkt_tab to /home/kudsit/nltk_data...
    [nltk_data]   Unzipping tokenizers/punkt_tab.zip.





    True




```python
import nltk
from nltk.tokenize import sent_tokenize

raw_text = "Hello world! How are you? I'm fine."
main_text = re.sub(r'[^a-zA-Z0-9\s]', '', text)

print(raw_text)
print(main_text)

sentences = sent_tokenize(main_text)

print(sentences)
```

    Hello world! How are you? I'm fine.
    Hello world How are you Im fine
    ['Hello world How are you Im fine']



```python
import requests 

from bs4 import BeautifulSoup

reponse = requests.get("https://www.autocarindia.com/car-news/bmw-m3-electric-due-in-2027-to-get-simulated-gearshifts-synthetic-sounds-438813")

raw_data = reponse.text

soup = BeautifulSoup(reponse.text, "html.parser")


text = soup.get_text(separator="\n", strip=True)
```


```python
print(text)
```

    BMW M3 Electric due in 2027 to get simulated gearshifts, synthetic sounds - Introduction | Autocar India
    Open menu
    Delhi
    Delhi
    Login / Register
    Find a car
    Find a bike
    News
    Reviews
    Features
    Galleries
    Sell Car
    Stories
    Advice
    Modern Classic Rally 2026
    Car News
    Follow us
    BMW M3 Electric due in 2027 to get simulated gearshifts, synthetic sounds
    Neue Klasse M car will get quad-motor setup.
    2 min read
    •
    15 Jan '26
    Dhruv Dhaka
    Previous slide
    Next slide
    BMW
    has confirmed that its first fully electric M car – an electric M3 based on the Neue Klasse EV platform – will feature simulated gearshifts and synthetic sounds. The company says this is aimed at giving the EV a more familiar and engaging driving feel.
    The electric M3 is due as early as the end of 2027 and will be based on the upcoming electric i3. BMW has not shared power output figures yet, but has made it clear that the car is being developed to maintain M’s reputation for driver-focused performance.
    Battery capacity to be at least 100kWh
    BMW hints a petrol M3 will continue alongside
    Quad-motor layout with one motor per wheel
    Simulated gearbox aimed at familiar M feel
    Dominik Suckart, BMW’s high-voltage battery chief, said to Autocar UK that the electric M3 has “a legacy to continue”. He also said BMW wants the platform to deliver a “familiar M driving experience”, even though it will be fully electric.
    That is the reason BMW is developing simulated gearshifts and sounds for the car. This is similar to approach taken by
    Hyundai
    in its Ioniq 5 N and Ioniq 6 N, which also use synthetic gearshifts and sound to make its performance EVs feel more involving.
    Quad motors and rear-drive modes confirmed
    BMW has confirmed the electric M3 will use four motors instead of the more common twin-motor setup used in Hyundais. The four motors will be connected to a single control unit, with an inverter and reduction gearbox for each wheel, along with torque vectoring.
    The M car will have a specific software stack called M Dynamic Performance Control, which, according to Suckart, will provide “never-seen-before handling and traction control.” This will give it the ability to switch from four-wheel drive to rear-wheel drive for track driving or drifting, as well as a rear-wheel-drive mode intended to help improve range.
    BMW said the electric M3 will get a battery with a capacity of at least 100kWh, designed to offer both high sustained performance and strong peak output with the ability to recuperate energy even under hard deceleration. The battery housing will form part of the car’s structure and will be attached to both the front and rear axles on the M3 version for added stiffness, unlike the standard i3, where it is only attached at the rear.
    BMW also confirmed that the M3 EV will use the ‘Heart of Joy’ high-performance control unit first shown on the BMW Vision Driving Experience concept. This unites all of the driving experience controls to enable faster and more intuitive reactions.
    Natural fibres to help control weight
    BMW has acknowledged that modern M cars are heavy and said it will use natural fibres in place of carbon fibre in some areas – as seen on the
    M4
    GT4 race car – to keep weight down where possible. Natural fibres produce a 40 percent lower CO2 emissions than carbon fibre.
    BMW has also strongly suggested that a petrol M3 will continue alongside the electric version, using an updated version of the B58 straight-six engine.
    Suggested News
    Mahindra issues statement on the BE 6 fire incident
    28 Jan '26
    Suraj Viswanathan
    2026 Renault Duster unveiled in India
    26 Jan '26
    Dipan Sur
    Upcoming Skoda launches in India in 2026
    20 Dec '25
    Uday Singh
    Lower-spec Tayron, more Golf GTIs among 5 Volkswagen launches in 2026
    29 Jan '26
    Lenny D'sa
    India EU FTA: European cars to get cheaper
    26 Jan '26
    Viraaj Bhatnagar
    2026 Renault Duster to get a strong-hybrid engine by Diwali
    26 Jan '26
    Ameya Dandekar
    Mahindra issues statement on the BE 6 fire incident
    28 Jan '26
    Suraj Viswanathan
    2026 Renault Duster unveiled in India
    26 Jan '26
    Dipan Sur
    Upcoming Skoda launches in India in 2026
    20 Dec '25
    Uday Singh
    Lower-spec Tayron, more Golf GTIs among 5 Volkswagen launches in 2026
    29 Jan '26
    Lenny D'sa
    India EU FTA: European cars to get cheaper
    26 Jan '26
    Viraaj Bhatnagar
    2026 Renault Duster to get a strong-hybrid engine by Diwali
    26 Jan '26
    Ameya Dandekar
    Kylaq accounts for nearly 40 percent of Skoda-VW group 2025 sales
    Sub-4m SUV sold over 45,000 units in 2025.
    2 min read
    •
    15 Jan '26
    Dhruv Dhaka
    Read full news
    2026 Modern Classic Car Rally to be held on January 31
    In its 4th edition, the Modern Classic Car Rally aims for more excitement and exhilaration this time.
    1 min read
    •
    14 Jan '26
    Zal Mavji
    Read full news
    Mahindra XEV 9S, XUV 7XO log 93,689 bookings combined on first day
    These translate into a booking value of over Rs 20,500 crore; XUV 7XO deliveries have already begun.
    1 min read
    •
    14 Jan '26
    Dhruv Dhaka
    Read full news
    JSW ties up with Chery to launch Jetour T2 in India
    The T2 will arrive as a locally assembled model with a plug-in hybrid powertrain and will carry a JSW badge.
    2 min read
    •
    14 Jan '26
    Sergius Barretto
    Read full news
    “We won’t get into a price war”: Mercedes Benz India MD and CEO
    A 2.85 percent dip in sales has been attributed to the focus on more profitable segments over a discount-driven strategy to gain volumes.
    2 min read
    •
    14 Jan '26
    Hormazd Sorabjee
    Read full news
    Upcoming Cars
    Renault Bigster
    ₹ 14.00 - 18.00 Lakhs
    Expected price
    Leapmotor C10
    ₹ 25.00 - 30.00 Lakhs
    Expected price
    Audi New Q5
    ₹ 70.00 - 75.00 Lakhs
    Expected price
    Leapmotor T03
    ₹ 8.00 - 12.00 Lakhs
    Expected price
    View all upcoming cars
    Trending Cars
    Renault Duster
    ₹ 10.00 - 20.00 Lakhs
    Expected price
    Tata Sierra
    ₹ 13.37 - 25.28 Lakhs
    On road price in delhi
    JSW Motors Jetour T2
    ₹ 15.00 - 30.00 Lakhs
    Expected price
    Tata Punch
    ₹ 6.22 - 12.30 Lakhs
    On road price in delhi
    Kia Seltos
    ₹ 12.79 - 23.64 Lakhs
    On road price in delhi
    Latest Cars
    Tata Punch
    ₹ 6.22 - 12.30 Lakhs
    On road price in delhi
    Mahindra XUV 3XO EV
    ₹ 14.74 - 15.86 Lakhs
    On road price in delhi
    View all latest cars
    Can't decide which car to buy?
    Ask our experts and get answers to all your car related queries.
    Ask experts
    Upcoming Cars
    Renault Bigster
    ₹ 14.00 - 18.00 Lakhs
    Expected price
    Leapmotor C10
    ₹ 25.00 - 30.00 Lakhs
    Expected price
    Audi New Q5
    ₹ 70.00 - 75.00 Lakhs
    Expected price
    Leapmotor T03
    ₹ 8.00 - 12.00 Lakhs
    Expected price
    Previous slide
    Next slide
    View all upcoming cars
    Trending Cars
    Renault Duster
    ₹ 10.00 - 20.00 Lakhs
    Expected price
    Tata Sierra
    ₹ 13.37 - 25.28 Lakhs
    On road price in delhi
    JSW Motors Jetour T2
    ₹ 15.00 - 30.00 Lakhs
    Expected price
    Tata Punch
    ₹ 6.22 - 12.30 Lakhs
    On road price in delhi
    Kia Seltos
    ₹ 12.79 - 23.64 Lakhs
    On road price in delhi
    Previous slide
    Next slide
    Latest Cars
    Tata Punch
    ₹ 6.22 - 12.30 Lakhs
    On road price in delhi
    Mahindra XUV 3XO EV
    ₹ 14.74 - 15.86 Lakhs
    On road price in delhi
    Previous slide
    Next slide
    View all latest cars
    Can't decide which car to buy?
    Ask our experts and get answers to all your car related queries.
    Ask experts
    Home
    car news
    bmw m3 electric due in 2027 to get simulated gearshifts synthetic sounds 438813
    Cars
    New cars
    Upcoming Cars
    Car reviews
    Car news
    Car loan calculator
    Bikes
    New bikes
    Upcoming bikes
    Bike reviews
    Bike news
    Bike loan calculator
    Others
    Ask Autocar anything
    Blogs
    Sitemap
    Contact us
    Sell Car
    Company
    About Us
    Our team
    Privacy policy
    Terms and conditions
    Advertise with us
    Stay Connected
    Our brands
    Copyright © 2026 Autocar India. All Rights Reserved.
    Made by team
    Autocar India
    with



```python
import unicodedata
import regex as re

## remove and clean text 
text = unicodedata.normalize("NFKC", text)
# text = re.sub(r'[^\p{L}\p{N}\s]', ' ', text)
raw_text = re.sub(r'[^a-zA-Z0-9\s]', '', text)

main_text_1 = re.sub(r'[\n\t\r]+', ' ', raw_text)

# Remove non-letter/number characters
main_text_2 = re.sub(r'[^\p{L}\p{N}\s]', ' ', main_text_1)

# Collapse multiple spaces
major_text = re.sub(r'\s+', ' ',main_text_2).strip()

print(major_text)
```

    BMW M3 Electric due in 2027 to get simulated gearshifts synthetic sounds Introduction Autocar India Open menu Delhi Delhi Login Register Find a car Find a bike News Reviews Features Galleries Sell Car Stories Advice Modern Classic Rally 2026 Car News Follow us BMW M3 Electric due in 2027 to get simulated gearshifts synthetic sounds Neue Klasse M car will get quadmotor setup 2 min read 15 Jan 26 Dhruv Dhaka Previous slide Next slide BMW has confirmed that its first fully electric M car an electric M3 based on the Neue Klasse EV platform will feature simulated gearshifts and synthetic sounds The company says this is aimed at giving the EV a more familiar and engaging driving feel The electric M3 is due as early as the end of 2027 and will be based on the upcoming electric i3 BMW has not shared power output figures yet but has made it clear that the car is being developed to maintain Ms reputation for driverfocused performance Battery capacity to be at least 100kWh BMW hints a petrol M3 will continue alongside Quadmotor layout with one motor per wheel Simulated gearbox aimed at familiar M feel Dominik Suckart BMWs highvoltage battery chief said to Autocar UK that the electric M3 has a legacy to continue He also said BMW wants the platform to deliver a familiar M driving experience even though it will be fully electric That is the reason BMW is developing simulated gearshifts and sounds for the car This is similar to approach taken by Hyundai in its Ioniq 5 N and Ioniq 6 N which also use synthetic gearshifts and sound to make its performance EVs feel more involving Quad motors and reardrive modes confirmed BMW has confirmed the electric M3 will use four motors instead of the more common twinmotor setup used in Hyundais The four motors will be connected to a single control unit with an inverter and reduction gearbox for each wheel along with torque vectoring The M car will have a specific software stack called M Dynamic Performance Control which according to Suckart will provide neverseenbefore handling and traction control This will give it the ability to switch from fourwheel drive to rearwheel drive for track driving or drifting as well as a rearwheeldrive mode intended to help improve range BMW said the electric M3 will get a battery with a capacity of at least 100kWh designed to offer both high sustained performance and strong peak output with the ability to recuperate energy even under hard deceleration The battery housing will form part of the cars structure and will be attached to both the front and rear axles on the M3 version for added stiffness unlike the standard i3 where it is only attached at the rear BMW also confirmed that the M3 EV will use the Heart of Joy highperformance control unit first shown on the BMW Vision Driving Experience concept This unites all of the driving experience controls to enable faster and more intuitive reactions Natural fibres to help control weight BMW has acknowledged that modern M cars are heavy and said it will use natural fibres in place of carbon fibre in some areas as seen on the M4 GT4 race car to keep weight down where possible Natural fibres produce a 40 percent lower CO2 emissions than carbon fibre BMW has also strongly suggested that a petrol M3 will continue alongside the electric version using an updated version of the B58 straightsix engine Suggested News Mahindra issues statement on the BE 6 fire incident 28 Jan 26 Suraj Viswanathan 2026 Renault Duster unveiled in India 26 Jan 26 Dipan Sur Upcoming Skoda launches in India in 2026 20 Dec 25 Uday Singh Lowerspec Tayron more Golf GTIs among 5 Volkswagen launches in 2026 29 Jan 26 Lenny Dsa India EU FTA European cars to get cheaper 26 Jan 26 Viraaj Bhatnagar 2026 Renault Duster to get a stronghybrid engine by Diwali 26 Jan 26 Ameya Dandekar Mahindra issues statement on the BE 6 fire incident 28 Jan 26 Suraj Viswanathan 2026 Renault Duster unveiled in India 26 Jan 26 Dipan Sur Upcoming Skoda launches in India in 2026 20 Dec 25 Uday Singh Lowerspec Tayron more Golf GTIs among 5 Volkswagen launches in 2026 29 Jan 26 Lenny Dsa India EU FTA European cars to get cheaper 26 Jan 26 Viraaj Bhatnagar 2026 Renault Duster to get a stronghybrid engine by Diwali 26 Jan 26 Ameya Dandekar Kylaq accounts for nearly 40 percent of SkodaVW group 2025 sales Sub4m SUV sold over 45000 units in 2025 2 min read 15 Jan 26 Dhruv Dhaka Read full news 2026 Modern Classic Car Rally to be held on January 31 In its 4th edition the Modern Classic Car Rally aims for more excitement and exhilaration this time 1 min read 14 Jan 26 Zal Mavji Read full news Mahindra XEV 9S XUV 7XO log 93689 bookings combined on first day These translate into a booking value of over Rs 20500 crore XUV 7XO deliveries have already begun 1 min read 14 Jan 26 Dhruv Dhaka Read full news JSW ties up with Chery to launch Jetour T2 in India The T2 will arrive as a locally assembled model with a plugin hybrid powertrain and will carry a JSW badge 2 min read 14 Jan 26 Sergius Barretto Read full news We wont get into a price war Mercedes Benz India MD and CEO A 285 percent dip in sales has been attributed to the focus on more profitable segments over a discountdriven strategy to gain volumes 2 min read 14 Jan 26 Hormazd Sorabjee Read full news Upcoming Cars Renault Bigster 1400 1800 Lakhs Expected price Leapmotor C10 2500 3000 Lakhs Expected price Audi New Q5 7000 7500 Lakhs Expected price Leapmotor T03 800 1200 Lakhs Expected price View all upcoming cars Trending Cars Renault Duster 1000 2000 Lakhs Expected price Tata Sierra 1337 2528 Lakhs On road price in delhi JSW Motors Jetour T2 1500 3000 Lakhs Expected price Tata Punch 622 1230 Lakhs On road price in delhi Kia Seltos 1279 2364 Lakhs On road price in delhi Latest Cars Tata Punch 622 1230 Lakhs On road price in delhi Mahindra XUV 3XO EV 1474 1586 Lakhs On road price in delhi View all latest cars Cant decide which car to buy Ask our experts and get answers to all your car related queries Ask experts Upcoming Cars Renault Bigster 1400 1800 Lakhs Expected price Leapmotor C10 2500 3000 Lakhs Expected price Audi New Q5 7000 7500 Lakhs Expected price Leapmotor T03 800 1200 Lakhs Expected price Previous slide Next slide View all upcoming cars Trending Cars Renault Duster 1000 2000 Lakhs Expected price Tata Sierra 1337 2528 Lakhs On road price in delhi JSW Motors Jetour T2 1500 3000 Lakhs Expected price Tata Punch 622 1230 Lakhs On road price in delhi Kia Seltos 1279 2364 Lakhs On road price in delhi Previous slide Next slide Latest Cars Tata Punch 622 1230 Lakhs On road price in delhi Mahindra XUV 3XO EV 1474 1586 Lakhs On road price in delhi Previous slide Next slide View all latest cars Cant decide which car to buy Ask our experts and get answers to all your car related queries Ask experts Home car news bmw m3 electric due in 2027 to get simulated gearshifts synthetic sounds 438813 Cars New cars Upcoming Cars Car reviews Car news Car loan calculator Bikes New bikes Upcoming bikes Bike reviews Bike news Bike loan calculator Others Ask Autocar anything Blogs Sitemap Contact us Sell Car Company About Us Our team Privacy policy Terms and conditions Advertise with us Stay Connected Our brands Copyright 2026 Autocar India All Rights Reserved Made by team Autocar India with



```python
# sentence tokenizations 
from nltk.tokenize import word_tokenize
sentences = word_tokenize(major_text)

print(sentences)
```

    ['BMW', 'M3', 'Electric', 'due', 'in', '2027', 'to', 'get', 'simulated', 'gearshifts', 'synthetic', 'sounds', 'Introduction', 'Autocar', 'India', 'Open', 'menu', 'Delhi', 'Delhi', 'Login', 'Register', 'Find', 'a', 'car', 'Find', 'a', 'bike', 'News', 'Reviews', 'Features', 'Galleries', 'Sell', 'Car', 'Stories', 'Advice', 'Modern', 'Classic', 'Rally', '2026', 'Car', 'News', 'Follow', 'us', 'BMW', 'M3', 'Electric', 'due', 'in', '2027', 'to', 'get', 'simulated', 'gearshifts', 'synthetic', 'sounds', 'Neue', 'Klasse', 'M', 'car', 'will', 'get', 'quadmotor', 'setup', '2', 'min', 'read', '15', 'Jan', '26', 'Dhruv', 'Dhaka', 'Previous', 'slide', 'Next', 'slide', 'BMW', 'has', 'confirmed', 'that', 'its', 'first', 'fully', 'electric', 'M', 'car', 'an', 'electric', 'M3', 'based', 'on', 'the', 'Neue', 'Klasse', 'EV', 'platform', 'will', 'feature', 'simulated', 'gearshifts', 'and', 'synthetic', 'sounds', 'The', 'company', 'says', 'this', 'is', 'aimed', 'at', 'giving', 'the', 'EV', 'a', 'more', 'familiar', 'and', 'engaging', 'driving', 'feel', 'The', 'electric', 'M3', 'is', 'due', 'as', 'early', 'as', 'the', 'end', 'of', '2027', 'and', 'will', 'be', 'based', 'on', 'the', 'upcoming', 'electric', 'i3', 'BMW', 'has', 'not', 'shared', 'power', 'output', 'figures', 'yet', 'but', 'has', 'made', 'it', 'clear', 'that', 'the', 'car', 'is', 'being', 'developed', 'to', 'maintain', 'Ms', 'reputation', 'for', 'driverfocused', 'performance', 'Battery', 'capacity', 'to', 'be', 'at', 'least', '100kWh', 'BMW', 'hints', 'a', 'petrol', 'M3', 'will', 'continue', 'alongside', 'Quadmotor', 'layout', 'with', 'one', 'motor', 'per', 'wheel', 'Simulated', 'gearbox', 'aimed', 'at', 'familiar', 'M', 'feel', 'Dominik', 'Suckart', 'BMWs', 'highvoltage', 'battery', 'chief', 'said', 'to', 'Autocar', 'UK', 'that', 'the', 'electric', 'M3', 'has', 'a', 'legacy', 'to', 'continue', 'He', 'also', 'said', 'BMW', 'wants', 'the', 'platform', 'to', 'deliver', 'a', 'familiar', 'M', 'driving', 'experience', 'even', 'though', 'it', 'will', 'be', 'fully', 'electric', 'That', 'is', 'the', 'reason', 'BMW', 'is', 'developing', 'simulated', 'gearshifts', 'and', 'sounds', 'for', 'the', 'car', 'This', 'is', 'similar', 'to', 'approach', 'taken', 'by', 'Hyundai', 'in', 'its', 'Ioniq', '5', 'N', 'and', 'Ioniq', '6', 'N', 'which', 'also', 'use', 'synthetic', 'gearshifts', 'and', 'sound', 'to', 'make', 'its', 'performance', 'EVs', 'feel', 'more', 'involving', 'Quad', 'motors', 'and', 'reardrive', 'modes', 'confirmed', 'BMW', 'has', 'confirmed', 'the', 'electric', 'M3', 'will', 'use', 'four', 'motors', 'instead', 'of', 'the', 'more', 'common', 'twinmotor', 'setup', 'used', 'in', 'Hyundais', 'The', 'four', 'motors', 'will', 'be', 'connected', 'to', 'a', 'single', 'control', 'unit', 'with', 'an', 'inverter', 'and', 'reduction', 'gearbox', 'for', 'each', 'wheel', 'along', 'with', 'torque', 'vectoring', 'The', 'M', 'car', 'will', 'have', 'a', 'specific', 'software', 'stack', 'called', 'M', 'Dynamic', 'Performance', 'Control', 'which', 'according', 'to', 'Suckart', 'will', 'provide', 'neverseenbefore', 'handling', 'and', 'traction', 'control', 'This', 'will', 'give', 'it', 'the', 'ability', 'to', 'switch', 'from', 'fourwheel', 'drive', 'to', 'rearwheel', 'drive', 'for', 'track', 'driving', 'or', 'drifting', 'as', 'well', 'as', 'a', 'rearwheeldrive', 'mode', 'intended', 'to', 'help', 'improve', 'range', 'BMW', 'said', 'the', 'electric', 'M3', 'will', 'get', 'a', 'battery', 'with', 'a', 'capacity', 'of', 'at', 'least', '100kWh', 'designed', 'to', 'offer', 'both', 'high', 'sustained', 'performance', 'and', 'strong', 'peak', 'output', 'with', 'the', 'ability', 'to', 'recuperate', 'energy', 'even', 'under', 'hard', 'deceleration', 'The', 'battery', 'housing', 'will', 'form', 'part', 'of', 'the', 'cars', 'structure', 'and', 'will', 'be', 'attached', 'to', 'both', 'the', 'front', 'and', 'rear', 'axles', 'on', 'the', 'M3', 'version', 'for', 'added', 'stiffness', 'unlike', 'the', 'standard', 'i3', 'where', 'it', 'is', 'only', 'attached', 'at', 'the', 'rear', 'BMW', 'also', 'confirmed', 'that', 'the', 'M3', 'EV', 'will', 'use', 'the', 'Heart', 'of', 'Joy', 'highperformance', 'control', 'unit', 'first', 'shown', 'on', 'the', 'BMW', 'Vision', 'Driving', 'Experience', 'concept', 'This', 'unites', 'all', 'of', 'the', 'driving', 'experience', 'controls', 'to', 'enable', 'faster', 'and', 'more', 'intuitive', 'reactions', 'Natural', 'fibres', 'to', 'help', 'control', 'weight', 'BMW', 'has', 'acknowledged', 'that', 'modern', 'M', 'cars', 'are', 'heavy', 'and', 'said', 'it', 'will', 'use', 'natural', 'fibres', 'in', 'place', 'of', 'carbon', 'fibre', 'in', 'some', 'areas', 'as', 'seen', 'on', 'the', 'M4', 'GT4', 'race', 'car', 'to', 'keep', 'weight', 'down', 'where', 'possible', 'Natural', 'fibres', 'produce', 'a', '40', 'percent', 'lower', 'CO2', 'emissions', 'than', 'carbon', 'fibre', 'BMW', 'has', 'also', 'strongly', 'suggested', 'that', 'a', 'petrol', 'M3', 'will', 'continue', 'alongside', 'the', 'electric', 'version', 'using', 'an', 'updated', 'version', 'of', 'the', 'B58', 'straightsix', 'engine', 'Suggested', 'News', 'Mahindra', 'issues', 'statement', 'on', 'the', 'BE', '6', 'fire', 'incident', '28', 'Jan', '26', 'Suraj', 'Viswanathan', '2026', 'Renault', 'Duster', 'unveiled', 'in', 'India', '26', 'Jan', '26', 'Dipan', 'Sur', 'Upcoming', 'Skoda', 'launches', 'in', 'India', 'in', '2026', '20', 'Dec', '25', 'Uday', 'Singh', 'Lowerspec', 'Tayron', 'more', 'Golf', 'GTIs', 'among', '5', 'Volkswagen', 'launches', 'in', '2026', '29', 'Jan', '26', 'Lenny', 'Dsa', 'India', 'EU', 'FTA', 'European', 'cars', 'to', 'get', 'cheaper', '26', 'Jan', '26', 'Viraaj', 'Bhatnagar', '2026', 'Renault', 'Duster', 'to', 'get', 'a', 'stronghybrid', 'engine', 'by', 'Diwali', '26', 'Jan', '26', 'Ameya', 'Dandekar', 'Mahindra', 'issues', 'statement', 'on', 'the', 'BE', '6', 'fire', 'incident', '28', 'Jan', '26', 'Suraj', 'Viswanathan', '2026', 'Renault', 'Duster', 'unveiled', 'in', 'India', '26', 'Jan', '26', 'Dipan', 'Sur', 'Upcoming', 'Skoda', 'launches', 'in', 'India', 'in', '2026', '20', 'Dec', '25', 'Uday', 'Singh', 'Lowerspec', 'Tayron', 'more', 'Golf', 'GTIs', 'among', '5', 'Volkswagen', 'launches', 'in', '2026', '29', 'Jan', '26', 'Lenny', 'Dsa', 'India', 'EU', 'FTA', 'European', 'cars', 'to', 'get', 'cheaper', '26', 'Jan', '26', 'Viraaj', 'Bhatnagar', '2026', 'Renault', 'Duster', 'to', 'get', 'a', 'stronghybrid', 'engine', 'by', 'Diwali', '26', 'Jan', '26', 'Ameya', 'Dandekar', 'Kylaq', 'accounts', 'for', 'nearly', '40', 'percent', 'of', 'SkodaVW', 'group', '2025', 'sales', 'Sub4m', 'SUV', 'sold', 'over', '45000', 'units', 'in', '2025', '2', 'min', 'read', '15', 'Jan', '26', 'Dhruv', 'Dhaka', 'Read', 'full', 'news', '2026', 'Modern', 'Classic', 'Car', 'Rally', 'to', 'be', 'held', 'on', 'January', '31', 'In', 'its', '4th', 'edition', 'the', 'Modern', 'Classic', 'Car', 'Rally', 'aims', 'for', 'more', 'excitement', 'and', 'exhilaration', 'this', 'time', '1', 'min', 'read', '14', 'Jan', '26', 'Zal', 'Mavji', 'Read', 'full', 'news', 'Mahindra', 'XEV', '9S', 'XUV', '7XO', 'log', '93689', 'bookings', 'combined', 'on', 'first', 'day', 'These', 'translate', 'into', 'a', 'booking', 'value', 'of', 'over', 'Rs', '20500', 'crore', 'XUV', '7XO', 'deliveries', 'have', 'already', 'begun', '1', 'min', 'read', '14', 'Jan', '26', 'Dhruv', 'Dhaka', 'Read', 'full', 'news', 'JSW', 'ties', 'up', 'with', 'Chery', 'to', 'launch', 'Jetour', 'T2', 'in', 'India', 'The', 'T2', 'will', 'arrive', 'as', 'a', 'locally', 'assembled', 'model', 'with', 'a', 'plugin', 'hybrid', 'powertrain', 'and', 'will', 'carry', 'a', 'JSW', 'badge', '2', 'min', 'read', '14', 'Jan', '26', 'Sergius', 'Barretto', 'Read', 'full', 'news', 'We', 'wont', 'get', 'into', 'a', 'price', 'war', 'Mercedes', 'Benz', 'India', 'MD', 'and', 'CEO', 'A', '285', 'percent', 'dip', 'in', 'sales', 'has', 'been', 'attributed', 'to', 'the', 'focus', 'on', 'more', 'profitable', 'segments', 'over', 'a', 'discountdriven', 'strategy', 'to', 'gain', 'volumes', '2', 'min', 'read', '14', 'Jan', '26', 'Hormazd', 'Sorabjee', 'Read', 'full', 'news', 'Upcoming', 'Cars', 'Renault', 'Bigster', '1400', '1800', 'Lakhs', 'Expected', 'price', 'Leapmotor', 'C10', '2500', '3000', 'Lakhs', 'Expected', 'price', 'Audi', 'New', 'Q5', '7000', '7500', 'Lakhs', 'Expected', 'price', 'Leapmotor', 'T03', '800', '1200', 'Lakhs', 'Expected', 'price', 'View', 'all', 'upcoming', 'cars', 'Trending', 'Cars', 'Renault', 'Duster', '1000', '2000', 'Lakhs', 'Expected', 'price', 'Tata', 'Sierra', '1337', '2528', 'Lakhs', 'On', 'road', 'price', 'in', 'delhi', 'JSW', 'Motors', 'Jetour', 'T2', '1500', '3000', 'Lakhs', 'Expected', 'price', 'Tata', 'Punch', '622', '1230', 'Lakhs', 'On', 'road', 'price', 'in', 'delhi', 'Kia', 'Seltos', '1279', '2364', 'Lakhs', 'On', 'road', 'price', 'in', 'delhi', 'Latest', 'Cars', 'Tata', 'Punch', '622', '1230', 'Lakhs', 'On', 'road', 'price', 'in', 'delhi', 'Mahindra', 'XUV', '3XO', 'EV', '1474', '1586', 'Lakhs', 'On', 'road', 'price', 'in', 'delhi', 'View', 'all', 'latest', 'cars', 'Cant', 'decide', 'which', 'car', 'to', 'buy', 'Ask', 'our', 'experts', 'and', 'get', 'answers', 'to', 'all', 'your', 'car', 'related', 'queries', 'Ask', 'experts', 'Upcoming', 'Cars', 'Renault', 'Bigster', '1400', '1800', 'Lakhs', 'Expected', 'price', 'Leapmotor', 'C10', '2500', '3000', 'Lakhs', 'Expected', 'price', 'Audi', 'New', 'Q5', '7000', '7500', 'Lakhs', 'Expected', 'price', 'Leapmotor', 'T03', '800', '1200', 'Lakhs', 'Expected', 'price', 'Previous', 'slide', 'Next', 'slide', 'View', 'all', 'upcoming', 'cars', 'Trending', 'Cars', 'Renault', 'Duster', '1000', '2000', 'Lakhs', 'Expected', 'price', 'Tata', 'Sierra', '1337', '2528', 'Lakhs', 'On', 'road', 'price', 'in', 'delhi', 'JSW', 'Motors', 'Jetour', 'T2', '1500', '3000', 'Lakhs', 'Expected', 'price', 'Tata', 'Punch', '622', '1230', 'Lakhs', 'On', 'road', 'price', 'in', 'delhi', 'Kia', 'Seltos', '1279', '2364', 'Lakhs', 'On', 'road', 'price', 'in', 'delhi', 'Previous', 'slide', 'Next', 'slide', 'Latest', 'Cars', 'Tata', 'Punch', '622', '1230', 'Lakhs', 'On', 'road', 'price', 'in', 'delhi', 'Mahindra', 'XUV', '3XO', 'EV', '1474', '1586', 'Lakhs', 'On', 'road', 'price', 'in', 'delhi', 'Previous', 'slide', 'Next', 'slide', 'View', 'all', 'latest', 'cars', 'Cant', 'decide', 'which', 'car', 'to', 'buy', 'Ask', 'our', 'experts', 'and', 'get', 'answers', 'to', 'all', 'your', 'car', 'related', 'queries', 'Ask', 'experts', 'Home', 'car', 'news', 'bmw', 'm3', 'electric', 'due', 'in', '2027', 'to', 'get', 'simulated', 'gearshifts', 'synthetic', 'sounds', '438813', 'Cars', 'New', 'cars', 'Upcoming', 'Cars', 'Car', 'reviews', 'Car', 'news', 'Car', 'loan', 'calculator', 'Bikes', 'New', 'bikes', 'Upcoming', 'bikes', 'Bike', 'reviews', 'Bike', 'news', 'Bike', 'loan', 'calculator', 'Others', 'Ask', 'Autocar', 'anything', 'Blogs', 'Sitemap', 'Contact', 'us', 'Sell', 'Car', 'Company', 'About', 'Us', 'Our', 'team', 'Privacy', 'policy', 'Terms', 'and', 'conditions', 'Advertise', 'with', 'us', 'Stay', 'Connected', 'Our', 'brands', 'Copyright', '2026', 'Autocar', 'India', 'All', 'Rights', 'Reserved', 'Made', 'by', 'team', 'Autocar', 'India', 'with']



```python
## stop words removal 

nltk.download('stopwords')
```

    [nltk_data] Downloading package stopwords to /home/kudsit/nltk_data...
    [nltk_data]   Unzipping corpora/stopwords.zip.





    True




```python
# stop words removal system 

from nltk.tokenize import word_tokenize
from nltk.corpus import stopwords

stop_words = set(stopwords.words('english'))

# remove stopwords + lowercase
clean_tokens = [
    t.lower() for t in sentences
    if t.lower() not in stop_words
]

print(clean_tokens)
```

    ['bmw', 'm3', 'electric', 'due', '2027', 'get', 'simulated', 'gearshifts', 'synthetic', 'sounds', 'introduction', 'autocar', 'india', 'open', 'menu', 'delhi', 'delhi', 'login', 'register', 'find', 'car', 'find', 'bike', 'news', 'reviews', 'features', 'galleries', 'sell', 'car', 'stories', 'advice', 'modern', 'classic', 'rally', '2026', 'car', 'news', 'follow', 'us', 'bmw', 'm3', 'electric', 'due', '2027', 'get', 'simulated', 'gearshifts', 'synthetic', 'sounds', 'neue', 'klasse', 'car', 'get', 'quadmotor', 'setup', '2', 'min', 'read', '15', 'jan', '26', 'dhruv', 'dhaka', 'previous', 'slide', 'next', 'slide', 'bmw', 'confirmed', 'first', 'fully', 'electric', 'car', 'electric', 'm3', 'based', 'neue', 'klasse', 'ev', 'platform', 'feature', 'simulated', 'gearshifts', 'synthetic', 'sounds', 'company', 'says', 'aimed', 'giving', 'ev', 'familiar', 'engaging', 'driving', 'feel', 'electric', 'm3', 'due', 'early', 'end', '2027', 'based', 'upcoming', 'electric', 'i3', 'bmw', 'shared', 'power', 'output', 'figures', 'yet', 'made', 'clear', 'car', 'developed', 'maintain', 'ms', 'reputation', 'driverfocused', 'performance', 'battery', 'capacity', 'least', '100kwh', 'bmw', 'hints', 'petrol', 'm3', 'continue', 'alongside', 'quadmotor', 'layout', 'one', 'motor', 'per', 'wheel', 'simulated', 'gearbox', 'aimed', 'familiar', 'feel', 'dominik', 'suckart', 'bmws', 'highvoltage', 'battery', 'chief', 'said', 'autocar', 'uk', 'electric', 'm3', 'legacy', 'continue', 'also', 'said', 'bmw', 'wants', 'platform', 'deliver', 'familiar', 'driving', 'experience', 'even', 'though', 'fully', 'electric', 'reason', 'bmw', 'developing', 'simulated', 'gearshifts', 'sounds', 'car', 'similar', 'approach', 'taken', 'hyundai', 'ioniq', '5', 'n', 'ioniq', '6', 'n', 'also', 'use', 'synthetic', 'gearshifts', 'sound', 'make', 'performance', 'evs', 'feel', 'involving', 'quad', 'motors', 'reardrive', 'modes', 'confirmed', 'bmw', 'confirmed', 'electric', 'm3', 'use', 'four', 'motors', 'instead', 'common', 'twinmotor', 'setup', 'used', 'hyundais', 'four', 'motors', 'connected', 'single', 'control', 'unit', 'inverter', 'reduction', 'gearbox', 'wheel', 'along', 'torque', 'vectoring', 'car', 'specific', 'software', 'stack', 'called', 'dynamic', 'performance', 'control', 'according', 'suckart', 'provide', 'neverseenbefore', 'handling', 'traction', 'control', 'give', 'ability', 'switch', 'fourwheel', 'drive', 'rearwheel', 'drive', 'track', 'driving', 'drifting', 'well', 'rearwheeldrive', 'mode', 'intended', 'help', 'improve', 'range', 'bmw', 'said', 'electric', 'm3', 'get', 'battery', 'capacity', 'least', '100kwh', 'designed', 'offer', 'high', 'sustained', 'performance', 'strong', 'peak', 'output', 'ability', 'recuperate', 'energy', 'even', 'hard', 'deceleration', 'battery', 'housing', 'form', 'part', 'cars', 'structure', 'attached', 'front', 'rear', 'axles', 'm3', 'version', 'added', 'stiffness', 'unlike', 'standard', 'i3', 'attached', 'rear', 'bmw', 'also', 'confirmed', 'm3', 'ev', 'use', 'heart', 'joy', 'highperformance', 'control', 'unit', 'first', 'shown', 'bmw', 'vision', 'driving', 'experience', 'concept', 'unites', 'driving', 'experience', 'controls', 'enable', 'faster', 'intuitive', 'reactions', 'natural', 'fibres', 'help', 'control', 'weight', 'bmw', 'acknowledged', 'modern', 'cars', 'heavy', 'said', 'use', 'natural', 'fibres', 'place', 'carbon', 'fibre', 'areas', 'seen', 'm4', 'gt4', 'race', 'car', 'keep', 'weight', 'possible', 'natural', 'fibres', 'produce', '40', 'percent', 'lower', 'co2', 'emissions', 'carbon', 'fibre', 'bmw', 'also', 'strongly', 'suggested', 'petrol', 'm3', 'continue', 'alongside', 'electric', 'version', 'using', 'updated', 'version', 'b58', 'straightsix', 'engine', 'suggested', 'news', 'mahindra', 'issues', 'statement', '6', 'fire', 'incident', '28', 'jan', '26', 'suraj', 'viswanathan', '2026', 'renault', 'duster', 'unveiled', 'india', '26', 'jan', '26', 'dipan', 'sur', 'upcoming', 'skoda', 'launches', 'india', '2026', '20', 'dec', '25', 'uday', 'singh', 'lowerspec', 'tayron', 'golf', 'gtis', 'among', '5', 'volkswagen', 'launches', '2026', '29', 'jan', '26', 'lenny', 'dsa', 'india', 'eu', 'fta', 'european', 'cars', 'get', 'cheaper', '26', 'jan', '26', 'viraaj', 'bhatnagar', '2026', 'renault', 'duster', 'get', 'stronghybrid', 'engine', 'diwali', '26', 'jan', '26', 'ameya', 'dandekar', 'mahindra', 'issues', 'statement', '6', 'fire', 'incident', '28', 'jan', '26', 'suraj', 'viswanathan', '2026', 'renault', 'duster', 'unveiled', 'india', '26', 'jan', '26', 'dipan', 'sur', 'upcoming', 'skoda', 'launches', 'india', '2026', '20', 'dec', '25', 'uday', 'singh', 'lowerspec', 'tayron', 'golf', 'gtis', 'among', '5', 'volkswagen', 'launches', '2026', '29', 'jan', '26', 'lenny', 'dsa', 'india', 'eu', 'fta', 'european', 'cars', 'get', 'cheaper', '26', 'jan', '26', 'viraaj', 'bhatnagar', '2026', 'renault', 'duster', 'get', 'stronghybrid', 'engine', 'diwali', '26', 'jan', '26', 'ameya', 'dandekar', 'kylaq', 'accounts', 'nearly', '40', 'percent', 'skodavw', 'group', '2025', 'sales', 'sub4m', 'suv', 'sold', '45000', 'units', '2025', '2', 'min', 'read', '15', 'jan', '26', 'dhruv', 'dhaka', 'read', 'full', 'news', '2026', 'modern', 'classic', 'car', 'rally', 'held', 'january', '31', '4th', 'edition', 'modern', 'classic', 'car', 'rally', 'aims', 'excitement', 'exhilaration', 'time', '1', 'min', 'read', '14', 'jan', '26', 'zal', 'mavji', 'read', 'full', 'news', 'mahindra', 'xev', '9s', 'xuv', '7xo', 'log', '93689', 'bookings', 'combined', 'first', 'day', 'translate', 'booking', 'value', 'rs', '20500', 'crore', 'xuv', '7xo', 'deliveries', 'already', 'begun', '1', 'min', 'read', '14', 'jan', '26', 'dhruv', 'dhaka', 'read', 'full', 'news', 'jsw', 'ties', 'chery', 'launch', 'jetour', 't2', 'india', 't2', 'arrive', 'locally', 'assembled', 'model', 'plugin', 'hybrid', 'powertrain', 'carry', 'jsw', 'badge', '2', 'min', 'read', '14', 'jan', '26', 'sergius', 'barretto', 'read', 'full', 'news', 'wont', 'get', 'price', 'war', 'mercedes', 'benz', 'india', 'md', 'ceo', '285', 'percent', 'dip', 'sales', 'attributed', 'focus', 'profitable', 'segments', 'discountdriven', 'strategy', 'gain', 'volumes', '2', 'min', 'read', '14', 'jan', '26', 'hormazd', 'sorabjee', 'read', 'full', 'news', 'upcoming', 'cars', 'renault', 'bigster', '1400', '1800', 'lakhs', 'expected', 'price', 'leapmotor', 'c10', '2500', '3000', 'lakhs', 'expected', 'price', 'audi', 'new', 'q5', '7000', '7500', 'lakhs', 'expected', 'price', 'leapmotor', 't03', '800', '1200', 'lakhs', 'expected', 'price', 'view', 'upcoming', 'cars', 'trending', 'cars', 'renault', 'duster', '1000', '2000', 'lakhs', 'expected', 'price', 'tata', 'sierra', '1337', '2528', 'lakhs', 'road', 'price', 'delhi', 'jsw', 'motors', 'jetour', 't2', '1500', '3000', 'lakhs', 'expected', 'price', 'tata', 'punch', '622', '1230', 'lakhs', 'road', 'price', 'delhi', 'kia', 'seltos', '1279', '2364', 'lakhs', 'road', 'price', 'delhi', 'latest', 'cars', 'tata', 'punch', '622', '1230', 'lakhs', 'road', 'price', 'delhi', 'mahindra', 'xuv', '3xo', 'ev', '1474', '1586', 'lakhs', 'road', 'price', 'delhi', 'view', 'latest', 'cars', 'cant', 'decide', 'car', 'buy', 'ask', 'experts', 'get', 'answers', 'car', 'related', 'queries', 'ask', 'experts', 'upcoming', 'cars', 'renault', 'bigster', '1400', '1800', 'lakhs', 'expected', 'price', 'leapmotor', 'c10', '2500', '3000', 'lakhs', 'expected', 'price', 'audi', 'new', 'q5', '7000', '7500', 'lakhs', 'expected', 'price', 'leapmotor', 't03', '800', '1200', 'lakhs', 'expected', 'price', 'previous', 'slide', 'next', 'slide', 'view', 'upcoming', 'cars', 'trending', 'cars', 'renault', 'duster', '1000', '2000', 'lakhs', 'expected', 'price', 'tata', 'sierra', '1337', '2528', 'lakhs', 'road', 'price', 'delhi', 'jsw', 'motors', 'jetour', 't2', '1500', '3000', 'lakhs', 'expected', 'price', 'tata', 'punch', '622', '1230', 'lakhs', 'road', 'price', 'delhi', 'kia', 'seltos', '1279', '2364', 'lakhs', 'road', 'price', 'delhi', 'previous', 'slide', 'next', 'slide', 'latest', 'cars', 'tata', 'punch', '622', '1230', 'lakhs', 'road', 'price', 'delhi', 'mahindra', 'xuv', '3xo', 'ev', '1474', '1586', 'lakhs', 'road', 'price', 'delhi', 'previous', 'slide', 'next', 'slide', 'view', 'latest', 'cars', 'cant', 'decide', 'car', 'buy', 'ask', 'experts', 'get', 'answers', 'car', 'related', 'queries', 'ask', 'experts', 'home', 'car', 'news', 'bmw', 'm3', 'electric', 'due', '2027', 'get', 'simulated', 'gearshifts', 'synthetic', 'sounds', '438813', 'cars', 'new', 'cars', 'upcoming', 'cars', 'car', 'reviews', 'car', 'news', 'car', 'loan', 'calculator', 'bikes', 'new', 'bikes', 'upcoming', 'bikes', 'bike', 'reviews', 'bike', 'news', 'bike', 'loan', 'calculator', 'others', 'ask', 'autocar', 'anything', 'blogs', 'sitemap', 'contact', 'us', 'sell', 'car', 'company', 'us', 'team', 'privacy', 'policy', 'terms', 'conditions', 'advertise', 'us', 'stay', 'connected', 'brands', 'copyright', '2026', 'autocar', 'india', 'rights', 'reserved', 'made', 'team', 'autocar', 'india']



```python

```


```python
len(clean_tokens)
```




    971




```python
### stemming 

from nltk.stem import PorterStemmer
#from nltk.stem import LancasterStemmer
```


```python
ps = PorterStemmer()

stemmed_tokens = [ps.stem(t) for t in clean_tokens]
print(stemmed_tokens)
```

    ['bmw', 'm3', 'electr', 'due', '2027', 'get', 'simul', 'gearshift', 'synthet', 'sound', 'introduct', 'autocar', 'india', 'open', 'menu', 'delhi', 'delhi', 'login', 'regist', 'find', 'car', 'find', 'bike', 'news', 'review', 'featur', 'galleri', 'sell', 'car', 'stori', 'advic', 'modern', 'classic', 'ralli', '2026', 'car', 'news', 'follow', 'us', 'bmw', 'm3', 'electr', 'due', '2027', 'get', 'simul', 'gearshift', 'synthet', 'sound', 'neue', 'klass', 'car', 'get', 'quadmotor', 'setup', '2', 'min', 'read', '15', 'jan', '26', 'dhruv', 'dhaka', 'previou', 'slide', 'next', 'slide', 'bmw', 'confirm', 'first', 'fulli', 'electr', 'car', 'electr', 'm3', 'base', 'neue', 'klass', 'ev', 'platform', 'featur', 'simul', 'gearshift', 'synthet', 'sound', 'compani', 'say', 'aim', 'give', 'ev', 'familiar', 'engag', 'drive', 'feel', 'electr', 'm3', 'due', 'earli', 'end', '2027', 'base', 'upcom', 'electr', 'i3', 'bmw', 'share', 'power', 'output', 'figur', 'yet', 'made', 'clear', 'car', 'develop', 'maintain', 'ms', 'reput', 'driverfocus', 'perform', 'batteri', 'capac', 'least', '100kwh', 'bmw', 'hint', 'petrol', 'm3', 'continu', 'alongsid', 'quadmotor', 'layout', 'one', 'motor', 'per', 'wheel', 'simul', 'gearbox', 'aim', 'familiar', 'feel', 'dominik', 'suckart', 'bmw', 'highvoltag', 'batteri', 'chief', 'said', 'autocar', 'uk', 'electr', 'm3', 'legaci', 'continu', 'also', 'said', 'bmw', 'want', 'platform', 'deliv', 'familiar', 'drive', 'experi', 'even', 'though', 'fulli', 'electr', 'reason', 'bmw', 'develop', 'simul', 'gearshift', 'sound', 'car', 'similar', 'approach', 'taken', 'hyundai', 'ioniq', '5', 'n', 'ioniq', '6', 'n', 'also', 'use', 'synthet', 'gearshift', 'sound', 'make', 'perform', 'ev', 'feel', 'involv', 'quad', 'motor', 'reardriv', 'mode', 'confirm', 'bmw', 'confirm', 'electr', 'm3', 'use', 'four', 'motor', 'instead', 'common', 'twinmotor', 'setup', 'use', 'hyundai', 'four', 'motor', 'connect', 'singl', 'control', 'unit', 'invert', 'reduct', 'gearbox', 'wheel', 'along', 'torqu', 'vector', 'car', 'specif', 'softwar', 'stack', 'call', 'dynam', 'perform', 'control', 'accord', 'suckart', 'provid', 'neverseenbefor', 'handl', 'traction', 'control', 'give', 'abil', 'switch', 'fourwheel', 'drive', 'rearwheel', 'drive', 'track', 'drive', 'drift', 'well', 'rearwheeldr', 'mode', 'intend', 'help', 'improv', 'rang', 'bmw', 'said', 'electr', 'm3', 'get', 'batteri', 'capac', 'least', '100kwh', 'design', 'offer', 'high', 'sustain', 'perform', 'strong', 'peak', 'output', 'abil', 'recuper', 'energi', 'even', 'hard', 'deceler', 'batteri', 'hous', 'form', 'part', 'car', 'structur', 'attach', 'front', 'rear', 'axl', 'm3', 'version', 'ad', 'stiff', 'unlik', 'standard', 'i3', 'attach', 'rear', 'bmw', 'also', 'confirm', 'm3', 'ev', 'use', 'heart', 'joy', 'highperform', 'control', 'unit', 'first', 'shown', 'bmw', 'vision', 'drive', 'experi', 'concept', 'unit', 'drive', 'experi', 'control', 'enabl', 'faster', 'intuit', 'reaction', 'natur', 'fibr', 'help', 'control', 'weight', 'bmw', 'acknowledg', 'modern', 'car', 'heavi', 'said', 'use', 'natur', 'fibr', 'place', 'carbon', 'fibr', 'area', 'seen', 'm4', 'gt4', 'race', 'car', 'keep', 'weight', 'possibl', 'natur', 'fibr', 'produc', '40', 'percent', 'lower', 'co2', 'emiss', 'carbon', 'fibr', 'bmw', 'also', 'strongli', 'suggest', 'petrol', 'm3', 'continu', 'alongsid', 'electr', 'version', 'use', 'updat', 'version', 'b58', 'straightsix', 'engin', 'suggest', 'news', 'mahindra', 'issu', 'statement', '6', 'fire', 'incid', '28', 'jan', '26', 'suraj', 'viswanathan', '2026', 'renault', 'duster', 'unveil', 'india', '26', 'jan', '26', 'dipan', 'sur', 'upcom', 'skoda', 'launch', 'india', '2026', '20', 'dec', '25', 'uday', 'singh', 'lowerspec', 'tayron', 'golf', 'gti', 'among', '5', 'volkswagen', 'launch', '2026', '29', 'jan', '26', 'lenni', 'dsa', 'india', 'eu', 'fta', 'european', 'car', 'get', 'cheaper', '26', 'jan', '26', 'viraaj', 'bhatnagar', '2026', 'renault', 'duster', 'get', 'stronghybrid', 'engin', 'diwali', '26', 'jan', '26', 'ameya', 'dandekar', 'mahindra', 'issu', 'statement', '6', 'fire', 'incid', '28', 'jan', '26', 'suraj', 'viswanathan', '2026', 'renault', 'duster', 'unveil', 'india', '26', 'jan', '26', 'dipan', 'sur', 'upcom', 'skoda', 'launch', 'india', '2026', '20', 'dec', '25', 'uday', 'singh', 'lowerspec', 'tayron', 'golf', 'gti', 'among', '5', 'volkswagen', 'launch', '2026', '29', 'jan', '26', 'lenni', 'dsa', 'india', 'eu', 'fta', 'european', 'car', 'get', 'cheaper', '26', 'jan', '26', 'viraaj', 'bhatnagar', '2026', 'renault', 'duster', 'get', 'stronghybrid', 'engin', 'diwali', '26', 'jan', '26', 'ameya', 'dandekar', 'kylaq', 'account', 'nearli', '40', 'percent', 'skodavw', 'group', '2025', 'sale', 'sub4m', 'suv', 'sold', '45000', 'unit', '2025', '2', 'min', 'read', '15', 'jan', '26', 'dhruv', 'dhaka', 'read', 'full', 'news', '2026', 'modern', 'classic', 'car', 'ralli', 'held', 'januari', '31', '4th', 'edit', 'modern', 'classic', 'car', 'ralli', 'aim', 'excit', 'exhilar', 'time', '1', 'min', 'read', '14', 'jan', '26', 'zal', 'mavji', 'read', 'full', 'news', 'mahindra', 'xev', '9s', 'xuv', '7xo', 'log', '93689', 'book', 'combin', 'first', 'day', 'translat', 'book', 'valu', 'rs', '20500', 'crore', 'xuv', '7xo', 'deliveri', 'alreadi', 'begun', '1', 'min', 'read', '14', 'jan', '26', 'dhruv', 'dhaka', 'read', 'full', 'news', 'jsw', 'tie', 'cheri', 'launch', 'jetour', 't2', 'india', 't2', 'arriv', 'local', 'assembl', 'model', 'plugin', 'hybrid', 'powertrain', 'carri', 'jsw', 'badg', '2', 'min', 'read', '14', 'jan', '26', 'sergiu', 'barretto', 'read', 'full', 'news', 'wont', 'get', 'price', 'war', 'merced', 'benz', 'india', 'md', 'ceo', '285', 'percent', 'dip', 'sale', 'attribut', 'focu', 'profit', 'segment', 'discountdriven', 'strategi', 'gain', 'volum', '2', 'min', 'read', '14', 'jan', '26', 'hormazd', 'sorabje', 'read', 'full', 'news', 'upcom', 'car', 'renault', 'bigster', '1400', '1800', 'lakh', 'expect', 'price', 'leapmotor', 'c10', '2500', '3000', 'lakh', 'expect', 'price', 'audi', 'new', 'q5', '7000', '7500', 'lakh', 'expect', 'price', 'leapmotor', 't03', '800', '1200', 'lakh', 'expect', 'price', 'view', 'upcom', 'car', 'trend', 'car', 'renault', 'duster', '1000', '2000', 'lakh', 'expect', 'price', 'tata', 'sierra', '1337', '2528', 'lakh', 'road', 'price', 'delhi', 'jsw', 'motor', 'jetour', 't2', '1500', '3000', 'lakh', 'expect', 'price', 'tata', 'punch', '622', '1230', 'lakh', 'road', 'price', 'delhi', 'kia', 'selto', '1279', '2364', 'lakh', 'road', 'price', 'delhi', 'latest', 'car', 'tata', 'punch', '622', '1230', 'lakh', 'road', 'price', 'delhi', 'mahindra', 'xuv', '3xo', 'ev', '1474', '1586', 'lakh', 'road', 'price', 'delhi', 'view', 'latest', 'car', 'cant', 'decid', 'car', 'buy', 'ask', 'expert', 'get', 'answer', 'car', 'relat', 'queri', 'ask', 'expert', 'upcom', 'car', 'renault', 'bigster', '1400', '1800', 'lakh', 'expect', 'price', 'leapmotor', 'c10', '2500', '3000', 'lakh', 'expect', 'price', 'audi', 'new', 'q5', '7000', '7500', 'lakh', 'expect', 'price', 'leapmotor', 't03', '800', '1200', 'lakh', 'expect', 'price', 'previou', 'slide', 'next', 'slide', 'view', 'upcom', 'car', 'trend', 'car', 'renault', 'duster', '1000', '2000', 'lakh', 'expect', 'price', 'tata', 'sierra', '1337', '2528', 'lakh', 'road', 'price', 'delhi', 'jsw', 'motor', 'jetour', 't2', '1500', '3000', 'lakh', 'expect', 'price', 'tata', 'punch', '622', '1230', 'lakh', 'road', 'price', 'delhi', 'kia', 'selto', '1279', '2364', 'lakh', 'road', 'price', 'delhi', 'previou', 'slide', 'next', 'slide', 'latest', 'car', 'tata', 'punch', '622', '1230', 'lakh', 'road', 'price', 'delhi', 'mahindra', 'xuv', '3xo', 'ev', '1474', '1586', 'lakh', 'road', 'price', 'delhi', 'previou', 'slide', 'next', 'slide', 'view', 'latest', 'car', 'cant', 'decid', 'car', 'buy', 'ask', 'expert', 'get', 'answer', 'car', 'relat', 'queri', 'ask', 'expert', 'home', 'car', 'news', 'bmw', 'm3', 'electr', 'due', '2027', 'get', 'simul', 'gearshift', 'synthet', 'sound', '438813', 'car', 'new', 'car', 'upcom', 'car', 'car', 'review', 'car', 'news', 'car', 'loan', 'calcul', 'bike', 'new', 'bike', 'upcom', 'bike', 'bike', 'review', 'bike', 'news', 'bike', 'loan', 'calcul', 'other', 'ask', 'autocar', 'anyth', 'blog', 'sitemap', 'contact', 'us', 'sell', 'car', 'compani', 'us', 'team', 'privaci', 'polici', 'term', 'condit', 'advertis', 'us', 'stay', 'connect', 'brand', 'copyright', '2026', 'autocar', 'india', 'right', 'reserv', 'made', 'team', 'autocar', 'india']



```python
## lemmenizations 
from nltk.stem import WordNetLemmatizer
nltk.download('punkt')
nltk.download('wordnet')
nltk.download('omw-1.4')

```

    [nltk_data] Downloading package punkt to /home/kudsit/nltk_data...
    [nltk_data]   Package punkt is already up-to-date!
    [nltk_data] Downloading package wordnet to /home/kudsit/nltk_data...
    [nltk_data] Downloading package omw-1.4 to /home/kudsit/nltk_data...



```python

lemmatizer = WordNetLemmatizer()
lemmatized_words = [lemmatizer.lemmatize(word) for word in stemmed_tokens]
print(lemmatized_words)

```


```python
## we need -> pos tagging 
### parse  tree generations 


### write code for POS tagging and syntax generations 
```
