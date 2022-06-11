<template>
    <div class="backdrop">
        <div class="modal">
            <p>Modal Content</p>
        </div>
    </div>
</template>

<style>
.modal{
    width: 200px;
    padding: 20px;
    margin: 100px auto;
    background: white;
    border-radius: 10px;
}

.backdrop{
    top: 0;
    position: fixed;
    background: rgba(0,0,0,0.5);
    height: 100%;
    width: 100%;
}
</style>