<template>
<div class="rating-area">
    <input type="radio" id="star-5" name="rating" value="5">
    <label for="star-5" title="Оценка «5»"></label>	
    <input type="radio" id="star-4" name="rating" value="4">
    <label for="star-4" title="Оценка «4»"></label>    
    <input type="radio" id="star-3" name="rating" value="3">
    <label for="star-3" title="Оценка «3»"></label>  
    <input type="radio" id="star-2" name="rating" value="2">
    <label for="star-2" title="Оценка «2»"></label>    
    <input type="radio" id="star-1" name="rating" value="1">
    <label for="star-1" title="Оценка «1»"></label>
</div>
</template>
<script>
export default ({
    name: "Rating"
})
</script>
<style lang="scss">
.rating-area {
	overflow: hidden;
	width: 265px;
	margin: 0 auto;

  &:not(:checked) > input {
    display: none;
  }
  &:not(:checked) > label {
    float: right;
    width: 16px;
    padding: 0;
    cursor: pointer;
    font-size: 16px;
    line-height: 16px;
    color: #EDEDED;
    text-shadow: 1px 1px #bbb;
  }
  &:not(:checked) > label:before {
    content: '★';
  }
  & > input:checked ~ label {
    color: #DC780B;
    text-shadow: 1px 1px #c60;
  }
  &:not(:checked) > label:hover,
  &:not(:checked) > label:hover ~ label {
    color: #DC780B;
  }
  & > input:checked + label:hover,
  & > input:checked + label:hover ~ label,
  & > input:checked ~ label:hover,
  & > input:checked ~ label:hover ~ label,
  & > label:hover ~ input:checked ~ label {
    color: #DC780B;
    text-shadow: 1px 1px goldenrod;
  }
  & > label:active {
    position: relative;
  }
}
</style>
