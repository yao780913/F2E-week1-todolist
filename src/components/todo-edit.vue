<template>
<div>
    <div id="addTask">
        <fa-icon :icon="['fas', 'plus']"></fa-icon>
        <span>Add Task</span>
    </div>
    <div id="newTask">
        <div class="newTask-header">
            <fa-icon :icon="['far','check-square']"></fa-icon> 
            <input type="text" id='txtTitle' placeholder='Type Something Here...' />
            <span class='right'>    
                
                <fa-icon :icon="['far','star']"></fa-icon>
                <fa-icon :icon="['fas', 'pencil-alt']"></fa-icon>
                
            </span>
    
        </div>
    
        <div class="newTask-list">
    
            <div class="newTask-list-input">  
                <h3> <fa-icon :icon="['far', 'calendar-alt']"></fa-icon> Deadline</h3>
                <input type="text" placeholder="yyyy/MM/dd HH:mm">
            </div>
    
            <div class="newTask-list-input">
                <h3><fa-icon :icon="['far', 'file']"></fa-icon>File</h3>
                <label class='lblUpload' for="uploadFile"><fa-icon :icon="['fas', 'plus']"></fa-icon></label>
                <input type="file" id='uploadFile'>
            </div>
    
            <div class="newTask-list-input">
                <h3><fa-icon :icon="['far', 'comment-dots']"></fa-icon>Comment</h3>
                <textarea name="textarea" id="txtComment" placeholder='Type your memo here...'></textarea>
            </div>
    
        </div>
    
        <div class="newTask-btnList">
            <button><fa-icon :icon="['fas', 'times']"></fa-icon>Cancel</button>
            <button><fa-icon :icon="['fas', 'plus']"></fa-icon>Add Task</button>
        </div>
    
    
    
    </div>
</div>
</template>

<script>
export default {};
</script>

<style lang='scss'>
@import '../assets/all.scss';
@import '../assets/helpers/_variables.scss';

#addTask{
    background-color: $color-white;
    margin: 24px 0 ;
    height: 65px;
    line-height: 65px;
    width: 100%;
    border: 2px solid $color-grey;
    padding-left: 33px;
    * {
        color: $color-grey;
        font-size: $fz-title;
    }
    > span {
        margin-left: 5px;
    }
    &:hover {
        cursor: pointer;
    }
}

#newTask{
    background-color: $color-white-dark;
    margin-bottom: 24px;
    width: $width-content;
    
    
    .newTask-header{
        margin: 0;
        padding: 24px 32px;
        border-bottom: 2px solid $color-grey;
        > [class*="fa"] {
            color: $color-white;
            background-color: $color-white;
            font-size: 24px;
            margin-right: 16px;
        }
        #txtTitle{
            padding: 0;
            font-size: $fz-title;
            background-color: $color-white-dark;
            
        }
        .right{
            float: right;
            > [class*="fa"] {
                margin-left: 16px;
                font-size: $fz-title;
                &.fa-star-selected{
                    color: $color-orange;
                }
                &.fa-pencil-alt{
                    color: $color-blue-light;
                }
            
            }
        }
    }
    
    .newTask-list{
        padding: 24px 72px;
    
        .newTask-list-input {
            
            > h3{
                margin: 10px 0;
                > [class*="fa"] {
                    margin-right: 8px;
                }
            }
            > input {
                margin: {
                    left: 24px;
                    bottom: 8px;
                }
            }
            > .lblUpload{
                @include flex();
                width: 32px;
                height: 32px;
                margin-left: 24px;
                padding: 8px;
                background-color: $color-grey;
                color: $color-white;
                cursor: pointer;
            }
            > input[type="file"]{
                display: none;
            }
            > textarea {
                width: 100%;
                height: 120px;
            }
        }
    }
    
    .newTask-btnList{
        @include flex();
        margin: 0;
        padding: 0;
        width: 100%;
        height: 60px;
        > button {
            @include flex();
            margin: 0;
            padding: 0;
            border: none;
            width: 100%;
            height: 100%;
            font-size: $fz-title;
            cursor: pointer;
            &:nth-child(1){
                color: $color-red;
                background-color: $color-white;
                > [class*="fa"] {
                    font-size: 40px;
                    padding-right: 16px;
                }
            }
            &:nth-child(2){
                color: $color-white;
                background-color: $color-blue-light;
                > [class*="fa"] {
                    font-size: 40px;
                    padding-right: 16px;
                }
            }
        }
    }
}
</style>

