<template>
    <div class="wrapper">
        <div class="block">
            <h2 class="block_title">Post Your Requirements</h2>
            <p class="block_paragraph">Please fill the form below to receive a quote for workspace.<br>
                Please add all the details required.</p>
        </div>
        <div class="form">
            <div class="form_header">
                <h3 class="form_header_title">Contact details</h3>
                <p class="form_header_paragraph">Please fill your information so we can get in touch with you.</p>
            </div>
            <div class="form_item">
                <h4 class="form_item_title">Name</h4>
                <input-item
                    placeholder="Your Name"
                    v-model="name"
                >
                </input-item>
            </div>
            <div class="form_item">
                <h4 class="form_item_title">Phone Number</h4>
                <input-item
                    placeholder="(123) 456 - 7890"
                    v-model="phoneNumber"
                >
                </input-item>
            </div>
            <div class="form_item">
                <h4 class="form_item_title">Email</h4>
                <input-item
                    placeholder="Your Mail ID"
                    v-model="email"
                >
                </input-item>
            </div>
            <div class="form_item">
                <h4 class="form_item_title">Date</h4>
                <input-item
                    placeholder="dd - mm - yyyy"
                    v-model="date"
                >
                </input-item>
            </div>
        </div>
        <button-item
        @getData="getData"
        ></button-item>
    </div>
</template>


<script>
    import ButtonItem from '../UI/ButtonItem.vue' 
    import InputItem from '../UI/InputItem.vue'

export default {
    components: {ButtonItem, InputItem},
    data() {
        return {
            name: '',
            phoneNumber: '',
            email: '',
            date: ''
        }
    },
    methods: {
        getData() {
            let data = {
                name: this.name,
                phoneNumber: this.phoneNumber,
                email: this.email,
                date: this.date
            }
            console.log(data)
        }
    }
}
</script>



<style>
    .wrapper {
        display: flex;
        flex-direction: column;
        width: 100%;
        align-items: center;
        justify-content: center;
        gap: 30px;
    }
    .block {
        display: flex;
        flex-direction: column;
        align-items: center;
        justify-content: center;
    }
    .block_paragraph {
        text-align: center;
    }
    .block_title {
        font-family: DM Sans, sans-serif;
        font-size: 34px;
        font-weight: 700;
        color: rgba(23, 15, 73, 1);
    }
    .block_paragraph {
        font-family: DM Sans, sans-serif;
        font-size: 18px;
        font-weight: 500;
        color: rgba(111, 108, 144, 1);
    }
    .form_header_title {
        font-family: DM Sans, sans-serif;
        font-size: 24px;
        font-weight: 700;
        text-align: left;
        color: rgba(23, 15, 73, 1);
    }
    .form_header_paragraph {
        font-family: DM Sans, sans-serif;
        font-size: 18px;
        font-weight: 500;
        text-align: left;
        color: rgba(111, 108, 144, 1);
    }
    .form_item_title {
        font-family: DM Sans, sans-serif;
        font-size: 18px;
        font-weight: 500;
        text-align: left;
        color: rgba(23, 15, 73, 1);
    }
</style>