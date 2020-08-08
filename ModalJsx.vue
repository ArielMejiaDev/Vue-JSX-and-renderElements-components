<script>
export default {
    name: 'ModalJsx',
    props: {
        show: {
            type: Boolean,
            default: false
        },
        message: {
            type: String,
            required: true
        }
    },
    render() {
        return (this.show) ? <div class="modal">
            <p class="message">{this.message}</p>
            <button onClick={this.clickCancelHandler} class="btn">Cancel</button>
            <button onClick={this.clickOkHandler} class="btn">Ok</button>
        </div> : null
    },
    methods: {
        clickCancelHandler() {
            console.log('click cancel')
        },
        clickOkHandler() {
            console.log('click ok')
        }
    }
}
</script>