# Option1
```
less -N
```

## Example 1
*Command*
```
less -N technical/911report/chapter-1.txt
```
*output:*
```
      1 
      2         
      3                 
      4 "WE HAVE SOME PLANES"
      5 
      6     Tuesday, September 11, 2001, dawned temperate and nearly cloudless in the eastern Uni      6 ted States. Millions of men and women readied themselves for work. Some made their way to      6  the Twin Towers, the signature structures of the World Trade Center complex in New York       6 City. Others went to Arlington, Virginia, to the Pentagon. Across the Potomac River, the       6 United States Congress was back in session. At the other end of Pennsylvania Avenue, peop      6 le began to line up for a White House tour. In Sarasota, Florida, President George W. Bus      6 h went for an early morning run.
      7 
      8     For those heading to an airport, weather conditions could not have been better for a       8 safe and pleasant journey. Among the travelers were Mohamed Atta and Abdul Aziz al Omari,      8  who arrived at the airport in Portland, Maine.
      9 
     10 INSIDE THE FOUR FLIGHTS
     11 
     12 Boarding the Flights
...(Above is just part of the output, the entire ouput is too long)
```

## Example 2
*Command:*
```
less -N technical/biomed/1468-6708-3-1.txt
```
*Output:*
```
      1 
      2   
      3     
      4       
      5         Introduction
      6         Older adults are frequently counseled to lose weight,
      7         even though there is little evidence that overweight is
      8         associated with increased mortality in those over age 65.
      9         Six large controlled population-based studies of
     10         non-smoking older adults have investigated the association
     11         between body mass index (BMI) and mortality, controlling
     12         for relevant covariates [ 1 2 3 4 5 6 ] . All studies found
     13         excess risk for persons with very low BMI, but that persons
     14         with moderately high BMI had little or no extra risk except
     15         in certain small subsets. A review of 13 studies of older
     16         adults drew similar conclusions [ 7 ] .
     17         Many healthy older adults report gradual weight gain
     18         throughout adult life. It may be that a small amount of
     19         gradual weight gain is normative and associated with the
     20         most robust health as we age. It has been suggested that
     21         weight standards be adjusted upwards for age [ 8 ] . Such
     22         recommendations remain controversial, however, because the
```

## Example 3
*Command*
```
less -N technical/government/Alcohol_Problems/Session4-PDF.txt
```
*Output:*
```
      1 
      2 
      3 
      4 
      5 Session 4.
      6 Implementing Preventive Interventions in
      7 Emergency Medicine: Strategic Considerations
      8 
      9 Larry M. Gentilello, MD
     10 Individuals who may benefit from alcohol counseling are often
     11 unaware of their need for treatment. The provision of alcohol
     12 interventions in emergency departments (ED) may provide an
     13 opportunity to treat individuals who are currently not actively
     14 seeking such care. Due to their lack of awareness of their problem,
     15 these patients are unlikely to present for treatment on their
     16 own.
     17 Treatment does not need to be sought actively to be effective.1
     18 How-ever, motivation can facilitate treatment. Studies suggest that
     19 physicians can opportunistically capitalize on the motivating
     20 effects of acute injuries or medical conditions that require
     21 emergency care to convince patients of the need for behavior
     22 change.2 This process may identify patients who have not yet
```
This `-N` option is showing the line number of the file that is displayed by the `less` command. It is useful in the way that we can easily reference a specific lind using the line number. Since `less` is commonly used in large files, having line numbers for each line is really useful for referencing.


# Option 2
```
-X
```
## Example 1
*Command:*
```
less -X technical/911report/chapter-1.txt
```
*Output*
```
(base) Tinas-MacBook-Pro:15l-docsearch tinazhan$ less -X technical/911report/chapter-1.txt

        
                
"WE HAVE SOME PLANES"

    Tuesday, September 11, 2001, dawned temperate and nearly cloudless in the eastern United States. Millions of men and women readied themselves for work. Some made their way to the Twin Towers, the signature structures of the World Trade Center complex in New York City. Others went to Arlington, Virginia, to the Pentagon. Across the Potomac River, the United States Congress was back in session. At the other end of Pennsylvania Avenue, people began to line up for a White House tour. In Sarasota, Florida, President George W. Bush went for an early morning run.

    For those heading to an airport, weather conditions could not have been better for a safe and pleasant journey. Among the travelers were Mohamed Atta and Abdul Aziz al Omari, who arrived at the airport in Portland, Maine.

INSIDE THE FOUR FLIGHTS

Boarding the Flights

    Boston: American 11 and United 175. Atta and Omari boarded a 6:00 A.M. flight from Portland to Boston's Logan International Airport.
(base) Tinas-MacBook-Pro:15l-docsearch tinazhan$ 
```

## Example 2
*Command:*
```
less -X technical/biomed/
```
*Output*
```
(base) Tinas-MacBook-Pro:15l-docsearch tinazhan$ less -X technical/biomed/1468-6708-3-1.txt

  
    
      
        Introduction
        Older adults are frequently counseled to lose weight,
        even though there is little evidence that overweight is
        associated with increased mortality in those over age 65.
        Six large controlled population-based studies of
        non-smoking older adults have investigated the association
        between body mass index (BMI) and mortality, controlling
        for relevant covariates [ 1 2 3 4 5 6 ] . All studies found
        excess risk for persons with very low BMI, but that persons
        with moderately high BMI had little or no extra risk except
        in certain small subsets. A review of 13 studies of older
        adults drew similar conclusions [ 7 ] .
        Many healthy older adults report gradual weight gain
        throughout adult life. It may be that a small amount of
        gradual weight gain is normative and associated with the
        most robust health as we age. It has been suggested that
        weight standards be adjusted upwards for age [ 8 ] . Such
        recommendations remain controversial, however, because the
(base) Tinas-MacBook-Pro:15l-docsearch tinazhan$ 
```
## Example 3
*Command*
```
less -X technical/government/Alcohol_Problems/Session4-PDF.txt
```
*Output*
```
(base) Tinas-MacBook-Pro:15l-docsearch tinazhan$ less -X technical/government/Alcohol_Problems/Session4-PDF.txt




Session 4.
Implementing Preventive Interventions in
Emergency Medicine: Strategic Considerations

Larry M. Gentilello, MD
Individuals who may benefit from alcohol counseling are often
unaware of their need for treatment. The provision of alcohol
interventions in emergency departments (ED) may provide an
opportunity to treat individuals who are currently not actively
seeking such care. Due to their lack of awareness of their problem,
these patients are unlikely to present for treatment on their
own.
Treatment does not need to be sought actively to be effective.1
How-ever, motivation can facilitate treatment. Studies suggest that
physicians can opportunistically capitalize on the motivating
effects of acute injuries or medical conditions that require
emergency care to convince patients of the need for behavior
change.2 This process may identify patients who have not yet
...skipping...
environments may doubt the applicability of research done in
academic centers. He suggested we need research on how to get
physicians to screen in the emergency department. One of the ways
we get physicians to do this is to get JCAHO to require it.
Daniel Hungerford observed that the Richmond-Kotelchuck model
suggests that changes in practice result from effort applied to all
three elements of the model-political will, social strategy, and
knowledge base. It might seem that research activities apply only
to the knowledge base aspect of the model. However, important
research activities need to be carried out in all three elements of
the model.
Robert Woolard favored continuing intervention research in EDs.
He believed that the realities of our practice settings help drive
the development of new ways of delivering counseling, for example,
computer-based methods. While emergency physicians may not have the
time or interest, the patients do. He suggested that research in
trauma centers and EDs can help alcohol researchers learn more
about the interventions they have already developed and can even
lead to novel interventions.



(base) Tinas-MacBook-Pro:15l-docsearch tinazhan$ 
```

The `-X` command allow the text or contents displayed to remain on the screen after `less` exits. For the output of the example, I included the command line before and after the text displayed to show that the text remains on the screen after exits. If we need to refer to the contents of the file for the next command, it is useful to have the contents on the screen, so that we can direcly read the content while typing the next command. 


# Option 3
```
-p "(text to search)"
```
## Example 1
*Command*
```
less -p "Interagency" technical/911report/chapter-1.txt
```
*Output*
```
Interagency Collaboration. The FAA and NORAD had developed protocols for working together in the event of a hijacking. As they existed on 9/11, the protocols for the FAA to obtain military assistance from NORAD required multiple levels of notification and approval at the highest levels of government.

    FAA guidance to controllers on hijack procedures assumed that the aircraft pilot would notify the controller via radio or by"squawking"a transponder code of "7500"-the universal code for a hijack in progress. Controllers would notify their supervisors, who in turn would inform management all the way up to FAA headquarters in Washington. Headquarters had a hijack coordinator, who was the director of the FAA Office of Civil Aviation Security or his or her designate.

    If a hijack was confirmed, procedures called for the hijack coordinator on duty to contact the Pentagon's National Military Command Center (NMCC) and to ask for a military escort aircraft to follow the flight, report anything unusual, and aid search and rescue in the event of an emergency. The NMCC would then seek approval from the Office of the Secretary of Defense to provide military assistance. If approval was given, the orders would be transmitted down NORAD's chain of command.

    The NMCC would keep the FAA hijack coordinator up to date and help the FAA centers coordinate
 directly with the military. NORAD would receive tracking information for the hijacked aircraft e
ither from joint use radar or from the relevant FAA air traffic control facility. Every attempt w
ould be made to have the hijacked aircraft squawk 7500 to help NORAD track it.
```
## Example 2
*Command*
```
less -p "Conclusion" technical/biomed/1468-6708-3-1.txt
```
*Output*
```
        Conclusion
        Recommendations for desirable weight have been
        criticized for emphasizing mortality rather than health. We
        found associations between YHL and obesity that were not
        present in the mortality analysis, suggesting that YHL may
        be a more sensitive measure of the burden of obesity in
        older adults, especially for women. Future efforts to
        determine desirable weight guidelines should include
        measures of YHL. Using either YOL or YHL, however, we found
        no excess risk for older adults who would be classified as
        'overweight' by the NHLBI guidelines. This suggests using
        YHL as the outcome measure in clinical trials involving
        obese or underweight older adults, and discouraging trials
        that address older adults who are merely overweight.
      
      
        Competing interests
        None declared
      
      
        Abbreviations
        BMI Body mass index
```

## Example 3
*Command*
```
less -p "References" technical/government/Alcohol_Problems/Session4-PDF.txt
```
*Output*
```
References
1. Loneck B, Garrett JA, Banks SM. A comparison of the Johnson
Intervention with four other methods of referral to outpatient
treatment. Am J Drug Alcohol Abuse 1996;22:233-46.
2. Monti PM, Colby SM, Barnett NP, et al. Brief intervention
for harm reduction with alcohol-positive older adolescents in a
hospital emergency department. J Consult Clin Psychol
1999;67:989-94.
3. Gentilello LM, Rivara FP, Donovan, DM, et al. Alcohol
interventions in a trauma center as a means of reducing the risk of
injury recurrence. Ann Surg 1999;230:473-83.
4. Fleming MF, Barry KL, Manwill LB, et al. Brief physician
advice for problem drinkers: a randomized controlled trial in
community based primary care practices. JAMA 1997;277:1039-45.
5. World Health Organization Brief Intervention Study Group. A
cross national trial of brief interventions with heavy drinkers. Am
J Public Health 1996;86: 948-55.
6. Bien TH, Miller WR, Tonigan JS. Brief interventions for
alcohol problems: a review. Addiction 1993;88:315-35.
7. Wilk AI, Jensen NM, Havighurst TC. Meta-analysis of
randomized control trials addressing brief interventions in heavy
alcohol drinkers. J Gen Intern Med 1997;12:274-83.
```

The option `-p "(text to search)"` will display the contents starting with the first occurence of `text to search`. For example, `-p "Reference"` in example 3 displays the text starting with the first occurence of `Reference`. This option can be useful when you only want to read a specific portion of the file. Thus, you can use this option to skip through unwanted material in order to save time and effort to look for the specific element.