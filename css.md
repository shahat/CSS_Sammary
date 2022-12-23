 
 > author : mohamed elshahat 
 > Date : 2 / 12 /2022
 > topic : sammary of css from iti and anither courses
> css  is consederd the presentational language that helps you to add good apperance to 
       structure that made by the html 
       * and also for easy development to  make css and html seperate 
         to seperate the steructure from presentation 

#######################################################################

>> adding css to html 

   note that : 3 method to add link / add css to html 
     - inline using attribute style="" .  try to avoid 
     - internal or embeded : by using tage <style> .. when u have specific thing 
     - external : by using link which is better one  

#####################################################

>> css selectors 

- universal selector     [ * ] the weekest selector all element 
- tage name selector     [ type selector ]
- attribute selector     [ select element that have attribute ] // Ex : input [type="text"]{ } // here just apply the change only on the input that have atteribute type > text search more in attribute selector 
- class selector         [ . ]
- id selector            [ # ]
- inline style           [ style = "" ]  the highst selector 

#####################################################

>> another selector : 
 
 div p    >> this mean optain all p tags inside div 
 div > p  >> this mean get p that have direct parent is div 
 div + p  >> this mean get p that have div pefore it 
 div ~ p  >> this means get all p after div 
 p.className >> this mean get all p that have class 
 You can add more that one class for the same element 

#####################################################

>> pseudo elemnts selectors :  every element have 
 pesedo element 

 - div::after {                           // this will add red hello to the end of that dev content 
    content : "hellooo"; 
    color : red }  >>
 - div::before        {}                  // this will add red hello to
  the end of that dev content 
  
  >> note [ after , before : works only with the tages that contains contents not like the input ]

 - div::first-letter  {}              //obtain the first letter 
 - div::first-line    {}               // obtain first line 
 - div::selection     {}                // apply the change once you select 

 ###################################################

 >> each element has pseudo class selector [its like the element status ]  that discribe it  

 - div:hover          {}              // when u hover change the color [ sudo class ]
 - a:link             {}
 - a:visited          {}
 - a:active           {}
 - a:hover            {}
 - input:focus        {}
 - input:invalid      {}  // mostly used in validation see the following exaples 

   >> input:invalid+span.msg{visibality : visible}
   >> input:valid+span.msg{visibality : hidden}
 - Note : you can do your reseach and discribe more about this thing 


#####################################################

>> properties introduction >>
   
   css reset file u can add it to your project if u want to make my page 
     looks the same in defferant browsers safari firefox an chrome  
   link to this file https://meyerweb.com/eric/tools/css/reset/

#####################################################
> background 
 

background-img : url("");
background-repeat: no-repeat ;
background-attachment : fixed ;
background-position: left top
backgorund-cover : cover , contain 



#####################################################

>> the css box model 

 - padding 
 - margin
 - border 
 - width 
 - height : مينفعش انسب هايت للبيرينت اللى هوا فى الاساس داينمك 

 EX : <div class='parent'>
         <div class="child">child</div>
         </div>
         /*css*/
         .parent{
            height : 100%
         }
         .child {
            height : 100%  // مش هيحس بالبيرين لان البيرينت واخد نسه داينمك 
         }

 - box-sizing : borber-box ;             >> الخاصيه دى بتخلى البادنج والبوردر مياخخددوش من ال width

 - display : inline-block       
          >> this makes the element inline but have the same time the 
             proberity of the block element 
     like accepting height and width properities bcz inline elements cant 
        accept these properities  .


#####################################################


  ** Note that : 
  when you do margain to elements next to each other the total margin between two el
  ements is equal to the sum of margins of two elements 

  but in case of these two elements are verticaly listed the total margain is equal to the big margain  


#####################################################

  - hide elements 

        >> display : hidden; // this will make it hidden but it still has her place 
                is empty in view 
        >> display : non ; // it is totaly disapper 

   - Shorthand properties
      >> border : 10px solid gray;  //

   - make element in center horizonial
      >> margain : 0 auto;   


#####################################################
 
   - border image 

           border-image-source: url(""); / this will make image border 
           border-image-slice : 60 70 110 70 ; 
           border-image: url("")30/10/15 repeat  
           30 > slice
           10 > width
           15 > outsit
           repeat > repeat the part in the meadel  
   - border-image : linear-gradient(red , green) 30 ;    
     بيعمل بوردر عادى بس فيه تدرج الوان

#####################################################

css postioning  & layout  : 

     postion :  

       1 > static : default 

       2 > fixed  :    -  relative to the veiw port
                       - take out of the document flow

       3 > absolute :  -  relative to body / <html>
                       - take out the document flow

       4 > relative  : - relative to its normal location 
                       - remain in the normal document flow

      يبقا هناالفكسيد والابسليوت مبيحافظش على مجانهم انما الريلتف بيحافظ على مكانه 
      وبيشوف ماكنه الاصلى فين وبعد كدا يتحرك منه 
       5 > stiky   : 
        - بتحافظ على مكانها ولكن لما تغير الفيو بورت بتشوف هيا واخده بعد كام من الفيو بورت وتتحرك معاه 
       6 > inhert : inhert from the parent

 >>> Note that : there something called view port its related to what u see infront of u . 
 >>> Note that  once u give the element postion fixed and give it top : 20px it will be float  and its postion will be relative to the view port .


 ##################################################### 

 positioning parent and child 

- اولا : لو انتا مش مدي البيرنت بوزيشن فيعتبر اللى واخد استاتك بمعنى اخر ملوش علاقه بالتشايلد اللى جواه اللى واخدين بوزيشن
- ولو البيرنت خد بوزيشن غير استاتك بيبدا ياثر على التشايلد بتاعه 
 
 >> absolute positioning : 
           Case 1 ( parent element is not static) : 
               - the absolute positioned chiled element will be relative to its parent element 
           Case 2 (No parent / parent element is static ) {
            the absolute positioned child element will be relative to the page elementitself . and if the position of the child is fixed it will ignore the body 
           }

--------------------------------------

floating  floating element : 

   float : left ;
   float : right ; 
   
   لو العنصر واخد ديفولت ويدس هيتشال زي ما البراوزر اول ما بيقرا ال ديف بيديله ويدس 100 
   اول ما هياخد فلوت هتلاقيه خد بس على قد المحتوي اللى انتا كاتبه جواه فانتا لازم ترجع تديله ويدز و هايت 
  
   float : non ; > defult
   clear : both ; دى بتحل مشكله ان العناصر اللى جايه بعد الفلوت بتطلع فى اي مكان فاضى في الصفحه لان الفلوت مبيخليش العنصر حاجز مكان محدد 
   clear : left ;
   clear : right ; 
>> note that : لما بتضيف فلوت للعنصر العنصر بيطفو فىى الصفحه 
 فلو فيه محتوا جاى تحته بالتالى هتلاقيه طفا هوا كمان وجه فى المكان الفاضي 

 #####################################################  
>> CSS Layout 

 Display property :  


 - display : list-item ; >> for container >> this will add point next to the container as it a part of a list 
                     : >> for child this will add point like the container 
                     هنا ممكن تضيف حاجه كمان وهى list-style-position:inside || outside >> this control the cyrcle will apper inside our outside the container 

--------------------------------------------------------
 inside category 

 1 - display : table ; >> for the container see the examples to understand 
                      >> when u put display table it actualy affect on the content inside the table like it does not have again the default width 100 % but it will collabs to its content so u should give it a width 
    

               container >> display:table  [
                 * caption >>  display : table-caption; >> هنا هيطع الكابشن برا البوردر بتاع التابل بس لو شيلت 
                 * header  >>      
                              display : table .. for container 
                              display : table-caption >>cant 
                              -header >> display : table-header-group
                              -body >> display : table-row-group;
                                 * row : display : table-row ;
                                    * cell : display : table-cell
  



2 - display : flex ;    هنلاحظ انه بياثر فى الحاجه اللى جوا الcontianer 

   u should know that there is two axis  the 
    > row axis : from left to wright  (main axis )
    > cross axis : from top to bottom

   2.1 > flex container   وهى خصائص خاصه بالكونتينر 

            - align-content : distribution of space between and around content items along a flexbox's cross axis
                        
                        flex-start : lines packed to the start of the container
                        flex-end   : lines packed to the end of the container
                        center     : lines packed to the center of the container
                        space-between : lines evenly distributed; the first line is at the start of the container while the last one is at the end
                        space-around : lines evenly distributed with equal space between them
                        stretch (default) : lines stretch to take up the remaining space


            - align-items   : it controls the alignment of items on the [ Cross Axis ].  
                            : in Grid Layout, it controls the alignment of items on the Block Axis within their grid area.

                        * center : center items in cross axis 
                        * stretch : 
                        * start : start at the start of the cross axis
                        * end : start at the end of the cross axis
                        * base-line : all the content will be at the same line 

          to make the box at the center you need justify-content in the main axis and the align-items in the cross 


            - justify-content : [ main axis ]  

              * stretch : do nothing its default
              * center : it will center items in the middle of the row axis so be carfull when you put the flex-direction             
              * space-evenly : put spaces at the each side for all items 
              * space-between : but spaces just in the middle so the first and the last one no spaces معنى كدا ان الاول والاخير مفيش بينهم وبين البارند مسافات 
              * space around : but spaces equaly between each element
                 so the first and last element have distance between them and the container half distance between 
              * flex-start : beside each other from the start 
              * flex-end : beside each other from the start 
              * center : put them in the center 


         - flex-direction : 
                           * row; > default 
                           * column ; > the row direction it will be in the cross direction  
                          

         - flex-warp :  
                           * nowrap : default 
                           * wrap : this make items if the container cant fit all items width the last one will go down 
                           * wrap-reverse : this make cross axis start from bottom to top  so when doing wraping it will start from the left side              

         - flex-flow : it is a shortcut for [ flex-direction - flex-wrap]                     
                                 * flex-flow : row-reverse wrap ;


                  
   
   2.2 : flex item  : its properties more spesific for the items inside the 
                   - align-self : it have many options that but its control the align of one element 

                   - flex-basis : it work with the main axis 
                   so when it is row these property overwrite the width of this element  
                   and when main axis is a columnn these property 
                   overwrite the height of the element 

                   - flex-grow  : controll the grow spead of the item
                   - flex-shrink : control the shrink speed of the element 
                   - flex : grow shrink base ; 
                      so its a shortcut for the three proberity 
                      0 : default of grow  if 1 it will grow 
                      1 : default of the shrink if 0 it will not shrink 
                      auto : is the base that is mean it will take the same size of element in the main axis 



                   - order : you can control the order of the elements using it  its gowing with the main axis 

######################################################################


factors that control which css rule applies to a given html element 
   
   1- inhertance
    some properties inherted but another is not 
      color , background is example of  inherted 
      margin , padding is not inherted

   2- cascad  لو انتا عندك مجموعه استايل فانتا  اخر حاجه هيشوفها البراوز هى اخر حاجه هتتنفذ 

   3 - specifity calculations 

      كل ما كان السيليكت بتاعك محدد اكتر كل ما كل ما كان اقوي وهوا اللى هيتنفذ 