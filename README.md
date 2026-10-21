// 1- creating the header part :
let element_name = document.createElement('h1')
let element_name_txt = document.createTextNode('Abdelrhman Ahmed ')
let element_hr_line = document.createElement('hr')

    element_name.appendChild(element_name_txt)
    document.body.appendChild(element_name)
document.body.appendChild(element_hr_line)

// 2- creating the input box
let element_input_box_1 = document.createElement('input')
    element_input_box_1.type='text'
    element_input_box_1.placeholder='Enter data here..'
    document.body.appendChild(element_input_box_1)

// 3- submit button 

let element_submit_1 = document.createElement('input')
    element_submit_1.type='submit'
    element_submit_1.value='submit'
    document.body.appendChild(element_submit_1)

// 4- clear button 

let element_clear_1 = document.createElement('input')
    element_clear_1.type='reset'
    element_clear_1.value='clear'
    document.body.appendChild(element_clear_1)

document.body.appendChild(element_hr_line)

//5- txtbox 

let element_txt_box = document.createElement('textarea')
    element_txt_box.type='textarea'
    element_txt_box.readOnly='true'
    document.body.appendChild(element_txt_box)


//functions part : 


// submition function 


element_submit_1.addEventListener('click',function(){
    if (element_input_box_1.value=='')
        {alert('Enter valid data')}
    else{
        element_txt_box.value=element_input_box_1.value
    }
})

//clear_function 



element_clear_1.addEventListener('click',function(){
    if(element_input_box_1.value=='')
        {alert('Enter valid data')}
    else{
        element_txt_box.value=''
        element_input_box_1.value=''
    }
}
)

// Styling : 


element_name.style.textAlign='center'
element_name.style.backgroundColor='aqua'
element_name.style.backgroundSize='50px'

element_input_box_1.addEventListener('mouseenter',function()
    {
        element_input_box_1.style.cursor='pointer'
        element_input_box_1.style.color = 'green';
    element_input_box_1.style.border = '2px solid green';})

element_input_box_1.addEventListener('mouseleave',function(){
    element_input_box_1.style.color = ''
    element_input_box_1.style.border = ''
})

element_submit_1.addEventListener('mouseenter',function(){
    element_submit_1.style.cursor='pointer'
    element_submit_1.style.border = '2px solid red'
})

element_submit_1.addEventListener('mouseleave',function(){
    element_submit_1.style.border = ''
})

element_clear_1.addEventListener('mouseenter',function(){
    element_clear_1.style.cursor='pointer'
    element_clear_1.style.border = '2px solid red'
})
element_clear_1.addEventListener('mouseleave',function(){
    element_clear_1.style.border = ''
})

document.body.style.textAlign='center'
