<!DOCTYPE html>
<!--
To change this license header, choose License Headers in Project Properties.
To change this template file, choose Tools | Templates
and open the template in the editor.
-->
<html>
    <head>
        <title>TODO supply a title</title>
        <meta charset="UTF-8">
        <meta name="viewport" content="width=device-width, initial-scale=1.0">
        <script>
            window.CKEDITOR_BASEPATH = 'js/plugins/ckeditor/';
        </script>

        <script type="text/javascript" src="JS/plugins.js"></script>
        <script type="text/javascript" src="JS/class.js"></script>
        <script>
        
            
        var fieldArray = [];
        var options = [];
        options['headline'] = 'Create user';
        options['action'] = function(){
            console.log($('#username').val(), $('#usergroup').val(), $('#password').val(), $('#firstname').val(), $('#lastname').val());
            alert('Submitted');
        };
        options['buttonTitle'] = 'Save';
        
        
        var field0 = [];
        field0['caption'] = 'Username';
        field0['inputName'] = 'username';
        field0['type'] = 'text';
        fieldArray[0] = field0;
        
        var captions = ['admin', 'moderator', 'standard-user'];
        var group_ids = ['admin', 'moderator', 'standard-user'];
        
        var field1 = [];
        field1['caption'] = 'Usergroup';
        field1['inputName'] = 'usergroup';
        field1['values'] = group_ids;
        field1['captions'] = captions;
        field1['type'] = 'dropdown';
        fieldArray[1] = field1;
        
        var field2 = [];
        field2['caption'] = 'Firstname';
        field2['inputName'] = 'firstname';
        field2['type'] = 'text';
        fieldArray[2] = field2;
        
        var field3 = [];
        field3['caption'] = 'Lastname';
        field3['inputName'] = 'lastname';
        field3['type'] = 'text';
        fieldArray[3] = field3;
               
        var field4 = [];
        field4['caption'] = 'Password';
        field4['inputName'] = 'password';
        field4['type'] = 'password';
        fieldArray[4] = field4;
        
        var field5 = [];
        field5['caption'] = 'Repeat password';
        field5['inputName'] = 'repeat_password';
        field5['type'] = 'password';
        fieldArray[5] = field5;
        
        $(document).ready(function(){
            gui.createForm('#content',fieldArray, options);
        });
            
            
        </script>
    </head>
    <body>
        <div>TODO write content</div>
        <div id="content"></div>
    </body>
</html>
