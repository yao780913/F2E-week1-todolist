
<template>

    <ul id="todolist">
        <li class="list-item">
        <p class='row1'>
            <fa-icon :icon="['far','check-square']" class="fa-check-square-checked"></fa-icon> 
            
            <span class="title title-deleted">
                Type Something Here...
            </span>
            <span class='right'>
                <fa-icon :icon="['far','star']"></fa-icon> 
                <fa-icon :icon="['fas','pencil-alt']"></fa-icon> 
            </span>
        </p>
        <p class='row2'>
            <fa-icon :icon="['far','calendar-alt']"></fa-icon> 5/14
            <fa-icon :icon="['far','file']"></fa-icon> 
            <fa-icon :icon="['far','comment-dots']"></fa-icon> 
        </p>
        </li>
        <li class="list-item">
            <p class='row1'>
                <fa-icon :icon="['far','check-square']"></fa-icon> 
                <span class="title">
                    Type Something Here...
                </span>
                <span class='right'>
                    <fa-icon :icon="['far','star']" class='fa-star-selected'></fa-icon> 
                    <fa-icon :icon="['fas','pencil-alt']"></fa-icon> 
                </span>
            </p>
            <p class='row2'>
                <fa-icon :icon="['far','calendar-alt']">5/14</fa-icon> 
            <fa-icon :icon="['far','file']"></fa-icon> 
            <fa-icon :icon="['far','comment-dots']"></fa-icon> 
            </p>
        </li>
        <li class="list-item"></li>
        <li class="list-item"></li>
    </ul>
</template>

<script>
export default {
}
</script>

<style lang='scss' scoped>
@import '../assets/all.scss';
@import '../assets/helpers/_variables.scss';

ul#todolist{
    
    width: 100%;
    height: auto;
    // border: 1px solid red;
    margin: 0;
    padding: 0;
    
    > li {
        background-color: $color-white-dark;
        flex-direction: column;
        list-style: none;
        margin-bottom: 8px;
        height: 100px;
        padding: 24px 32px;
        > p {
            margin: 0;
            padding: 0;
            &.row1 {
                margin-bottom: 16px;
                
                .fa-check-square{
                    color: $color-white;
                    background-color: $color-white;
                    &.fa-check-square-checked{
                        background-color: $color-blue-light;
                    }
                }

                [class*="fa"] {
                    font-size: 20px;
                    
                }
                .title{
                    font-size: $fz-subTitle;
                    font-weight: bold;
                    height: 24px;
                    line-height: 24px;
                    &.title-deleted{
                        text-decoration: line-through;
                        color: $color-grey;
                    }
                }
                .right{
                    float: right;
                    right: 0;
                    > [class*="fa"] {
                        margin-left: 16px;
                    
                        &.fa-star-selected{
                            color: $color-orange;
                            
                        }
                    }
                }
            }
            &.row2 {
                > [class*="fa"]:nth-child(1){
                    margin-left: 20px;
                    
                }
                > [class*="fa"] {
                    font-size: 16px;
                    height: 16px;
                    margin: 0 4px;
                }
            }
        }
    }
}

</style>
