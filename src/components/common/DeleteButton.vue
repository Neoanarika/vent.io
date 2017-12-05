<template>
    <!-- Delete Button -->
    <button id="delete-button" class="is-radiusless">
        <i class="fa fa-trash-o"></i>
    </button><!-- End of Delete Button -->
</template>

<script>
export default {
  name: 'DeleteButton'
}
</script>

<style lang="scss" scoped>
    #delete-button {
        width: 3.5vw;
        height: 3.5vw;
        border: 0;
        background-color: whitesmoke;
        cursor: pointer;
    }

    #delete-button > i {
        font-size: 1.35rem;
    }

    #delete-button:hover {
        background-color: transparent;
    }

    #delete-button:hover > i {
        font-size: 1.5rem;
    }

    #delete-button:focus {
        outline: none;
    }
</style>
