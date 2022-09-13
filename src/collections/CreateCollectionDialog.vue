<template>
    <div>
        <el-dialog title="Collection" :visible.sync="dialogVisible">
            <StepComponent :steps="steps" :activite="activite"/>
            <div class="form-container">
                <el-form ref="form" :model="form" label-position="top" label-width="80px" style="text-align:left;">
                    <!-- <el-row :gutter="20">
                        <el-col :span=12 style="text-align: left;"> -->
                    <el-form-item label="Collection Name" style="padding: 0;">
                        <el-input style="width: 300px" size="small" v-model="form.name"></el-input>
                    </el-form-item>
                        <!-- </el-col>
                        <el-col :span=12 style="text-align: left;"> -->
                    <el-form-item label="Token Symbol" style="padding: 0;">
                        <el-input style="width: 100px" size="small" v-model="form.token"></el-input>
                    </el-form-item>
                        <!-- </el-col>
                    </el-row> -->
                    <el-form-item label="Select Network" style="padding: 0;">
                        <el-radio-group v-model="form.network">
                            <el-radio :label="1">Ethereum</el-radio>
                            <el-radio :label="2">Polygon</el-radio>
                        </el-radio-group>
                    </el-form-item>
                    <el-form-item label="Select Protocol Type" style="padding: 0;">
                        <el-radio-group v-model="form.protocol">
                            <el-radio :label="1">ERC712</el-radio>
                            <el-radio :label="2">ERC1155</el-radio>
                        </el-radio-group>
                    </el-form-item>
                </el-form>
                <div>
                    <el-button type="primary" size="small">Next</el-button>
                </div>
            </div>
        </el-dialog>
    </div>
</template>
<script>
import { STEPS } from './constant'
import StepComponent from '@/components/steps/StepComponent.vue'

export default {
    components: {
        StepComponent
    },
    data() {
        return {
            steps: STEPS,
            activite: 1,
            dialogVisible: false,
            form: {
                name: undefined,
                token: undefined,
                network: undefined,
                protocol: undefined
            }
        }
    },
    methods: {
        openDialog() {
            this.dialogVisible = true
        }
    },
}
</script>
<style scoped>
.form-container {
    margin-top: 30px;
}
</style>