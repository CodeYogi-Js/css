```html
<!-- :not(), :is(), :where(), :has() -->
<!DOCTYPE html>
<html lang="en">
    <head>
        <meta charset="UTF-8">
        <meta name="viewport" content="width=device-width, initial-scale=1.0">
        <title>not(), is(), where(), has()</title>
        <style>
            *{
                margin: 2px;
                padding: 0;
                box-sizing: border-box;
            }
            #parent{
                border: 2px solid blueviolet;
            }
            .box{
                height: 100px;
                width: 100px;
                border: 2px solid rgb(0, 128, 255);
                padding: 5px;
                margin-bottom: 20px;
            }

            /* #parent .box:not(:first-child){
                background-color: rgb(251, 200, 70);
            }
            #parent .box:not(:last-child){
                background-color: pink;
            } */

            /* #parent .box:not(:nth-child(1),:nth-child(4)){
                background-color: pink;
            } */
            /*is() lets you group many selectors together.
	         Instead of writing long repeated code, you can put them inside .*/
            #test1 h1,
            #test1 h2,
            #test1 h3{
                font-family: Arial, Helvetica, sans-serif;
            }
            #test1 :is(h1, h2, h3){
                background-color: aqua;
                margin: 2px;
            }
            :is(#test1, #test2) h2{
                background-color: brown;
            }
            :is(#test1, #test2) :is(h1,p){
                background-color: beige;
            }


            /*has speudo class*/
            /*The has() pseudo-class is used to apply styles on a parent element, but only if that parent meets a specific condition about its children (or nearby elements).*/
            /* #has-box div:has(h2){
                background-color: yellowgreen;
            }
            #has-box div:has(>h2){
                background-color: lightcoral;
            } */
             #has-box div:has(h2+ p){
                background-color: blue;
             }
             /*is and where work same but specificity is 0*/
        </style>
    </head>
    <body>
        <!--not speudo class-->
        <div id="parent">
            <div id="box1" class="box">box-1</div>
            <div id="box2" class="box">box-2</div>
            <div id="box3" class="box">box-3</div>
            <div id="box4" class="box">box-4</div>
        </div>
        <!--is pseudo class-->
        <div id="test1">
            <h1>section 1</h1>
            <h2>sub Heading</h2>
            <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Ad eius inventore rerum odio harum delectus est quo mollitia, incidunt nemo assumenda consequatur non ipsum quae ut id, in labore, iure soluta repellat. Et saepe enim deleniti aspernatur facilis possimus, nam omnis laudantium quis, repellendus distinctio vitae obcaecati unde eveniet soluta.</p>
            <h3>sub heading 2</h3>
            <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Ratione, impedit!</p>
        </div>
        <hr>
        <div id="test2">
            <h2>section Two</h2>
            <p>Lorem ipsum dolor, sit amet consectetur adipisicing elit. Cupiditate quae odit numquam in natus blanditiis doloribus, repellendus accusamus. Laudantium consequuntur sint adipisci, vitae voluptates fuga!</p>
        </div>
        <div id="has-box">
            <div>
                <section class="abc">
                    <h2>arindam baba</h2>
                </section>
            </div>
            <div>
                <h2>just testing</h2>
                <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Rerum, sequi!</p>
            </div>
            <div>
                <h3>just another testing</h3>
            </div>
        </div>
    </body>
</html>
```
