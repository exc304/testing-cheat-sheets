#### Test 1: ASCII Special Characters in UI
**Actions:**  
> *Create a new Object Cataloging record*  
> ***Add any number in Identification Number field.***  
>
>> Variation A: In one single and one multiline text area, copy and paste: `"This sentence is wrapped in double quotes."`  
>> Variation B: In one single and one multiline text area, copy and paste: `'single quotes'`  
>> Variation C: In one single and one multiline text area, copy and paste: `[square brackets]`  
>> Variation D: In one single and one multiline text area, copy and paste: `{curly braces}`  
>> Variation E: In one single and one multiline text area, copy and paste: `<angle brackets>`  
>> Variation F: In one single and one multiline text area, copy and paste: `<! -- XML comment -->`  
>> Variation H: In one single and one multiline text area, copy and paste: `"quoted" segment & ampersand`  
>> Variation I: In one single and one multiline text area, copy and paste: `"A "quoted" segment; & (entity); wrapped in quotes"`  
>> Variation J: In one single and one multiline text area, copy and paste: `backslashes and colon: \c:\mydocs`  
>> Variation L: In one single and one multiline text area, copy and paste: `hash: #20`  
>> Variation M: In one single and one multiline text area, copy and paste: `escaped slash: \/`
>
> Save the record  

**Expected: After the successful save message appears, all fields should contain the same value as you entered**

---

#### Test 2: Strings of over 500 characters
**Actions:**  
> *Continue from Test 1 (or open an existing Object cataloging record)*  
> ***In at least one text area (multiline text field), paste or enter text containing more than 500 characters.***  
>  
> Example:  
>> START  
>> 1) I am typing in more than 500 characters of text to test whether the more than 500 characters are cut off or if they display correctly. 500 >> characters is a lot of text.  
>> 2) I am typing in more than 500 characters of text to test whether the more than 500 characters are cut off or if they display correctly. 500 >> characters is a lot of text.  
>> 3) I am typing in more than 500 characters of text to test whether the more than 500 characters are cut off or if they display correctly. 500 >> characters is a lot of text.  
>> END
> 
> Save the record

**Expected: After the successful save message appears, text area should contain the same characters as you entered and should not be cut off**

---

### Test 3: Non-ASCII Characters in UI
**Actions:**
> *Continue from Test 2 (or open an existing Object cataloging record)*
> ***In one single and one multiline text area, copy and paste:*** `café`
>
>> ***In one single and one multiline text area, copy and paste:***
>>
>> | Be sure characters paste as shown      | 
>> | ----------- | 
>> | ñóǹ äŝçíì 汉语/漢語  华语/華語 Huáyǔ; 中文 Zhōngwén 漢字仮名交じり文 Lech Wałęsa æøå| 
>
> Save the record

**Expected: After the successful save message appears, all fields should contain the same value as you entered**


  
