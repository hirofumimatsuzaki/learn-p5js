<template>
    <div id="sampleProjectArea">
        <el-tabs :tab-position="tabPosition" style="height: 500px;">
            <el-tab-pane label="位置と大きさ">
                <el-row :gutter="10" type="flex" justify="space-around">
                    <el-col :span="5">
                        <SampleProjectButton id="1-1" title="正方形" @update-code="setCode"/>
                    </el-col>
                    <el-col :span="5">
                        <SampleProjectButton id="1-2" title="Movin' Square" @update-code="setCode"/>
                    </el-col>
                    <el-col :span="5">
                        <SampleProjectButton id="1-3" title="Mouse Interaction" @update-code="setCode"/>
                    </el-col>
                    <el-col :span="5">
                        <SampleProjectButton id="1-4" title="Width & Height" @update-code="setCode"/>
                    </el-col>
                </el-row>
            </el-tab-pane>
            <el-tab-pane label="Colors">
                <el-row :gutter="10" type="flex" justify="space-around">
                    <el-col :span="5">
                        <SampleProjectButton id="2-1" title="Gray scale" @update-code="setCode"/>
                    </el-col>
                    <el-col :span="5">
                        <SampleProjectButton id="2-2" title="Red, Green, Blue" @update-code="setCode"/>
                    </el-col>
                    <el-col :span="5">
                        <SampleProjectButton id="2-3" title="Hue, Saturation, Brightness" @update-code="setCode"/>
                    </el-col>
                    <el-col :span="5">
                        <SampleProjectButton id="2-4" title="CSS" @update-code="setCode"/>
                    </el-col>
                    <el-col :span="5">
                        <SampleProjectButton id="2-5" title="Alpha" @update-code="setCode"/>
                    </el-col>
                </el-row>
            </el-tab-pane>
            <el-tab-pane label="Shape editing">
                <el-row :gutter="10" type="flex" justify="space-around">
                    <el-col :span="5">
                        <SampleProjectButton id="3-1" title="Fill & Stroke" @update-code="setCode"/>
                    </el-col>
                    <el-col :span="5">
                        <SampleProjectButton id="3-2" title="Translation" @update-code="setCode"/>
                    </el-col>
                    <el-col :span="5">
                        <SampleProjectButton id="3-3" title="Rotation" @update-code="setCode"/>
                    </el-col>
                    <el-col :span="5">
                        <SampleProjectButton id="3-4" title="Scaling" @update-code="setCode"/>
                    </el-col>
                </el-row>
            </el-tab-pane>
            <el-tab-pane label="Devices">
                <el-row :gutter="10" type="flex" justify="space-around">
                    <el-col :span="5">
                        <SampleProjectButton id="4-1" title="Mouse Interaction 1" @update-code="setCode"/>
                    </el-col>
                    <el-col :span="5">
                        <SampleProjectButton id="4-2" title="Mouse Interaction 2" @update-code="setCode"/>
                    </el-col>
                    <el-col :span="5">
                        <SampleProjectButton id="4-3" title="Keyboard Interaction 1" @update-code="setCode"/>
                    </el-col>
                    <el-col :span="5">
                        <SampleProjectButton id="4-4" title="Keyboard Interaction 2" @update-code="setCode"/>
                    </el-col>
                </el-row>
            </el-tab-pane>
            <el-tab-pane label="Randomize">
                <el-row :gutter="10" type="flex" justify="space-around">
                    <el-col :span="5">
                        <SampleProjectButton id="5-1" title="Random Number 1" @update-code="setCode"/>
                    </el-col>
                    <el-col :span="5">
                        <SampleProjectButton id="5-2" title="Random Number 2" @update-code="setCode"/>
                    </el-col>
                    <el-col :span="5">
                        <SampleProjectButton id="5-3" title="Random Coloring 1" @update-code="setCode"/>
                    </el-col>
                    <el-col :span="5">
                        <SampleProjectButton id="5-4" title="Random Coloring 2" @update-code="setCode"/>
                    </el-col>
                </el-row>
            </el-tab-pane>
            <el-tab-pane label="Sin & Cos & DOM">
                <el-row :gutter="10" type="flex" justify="space-around">
                    <el-col :span="5">
                        <SampleProjectButton id="6-1" title="Sin & Cos Basic 1" @update-code="setCode"/>
                    </el-col>
                    <el-col :span="5">
                        <SampleProjectButton id="6-2" title="Sin & Cos Basic 2" @update-code="setCode"/>
                    </el-col>
                    <el-col :span="5">
                        <SampleProjectButton id="6-3" title="Mouseround" @update-code="setCode"/>
                    </el-col>
                    <el-col :span="5">
                        <SampleProjectButton id="6-4" title="Slider Interaction" @update-code="setCode"/>
                    </el-col>
                    <el-col :span="5">
                        <SampleProjectButton id="6-5" title="Button Interaction" @update-code="setCode"/>
                    </el-col>
                </el-row>
            </el-tab-pane>
            <el-tab-pane label="Further Step">
                <el-row :gutter="10" type="flex" justify="space-around">
                    <el-col :span="5">
                        <SampleProjectButton id="7-1" title="Trajectory" @update-code="setCode"/>
                    </el-col>
                    <el-col :span="5">
                        <SampleProjectButton id="7-2" title="Spotlight" @update-code="setCode"/>
                    </el-col>
                    <el-col :span="5">
                        <SampleProjectButton id="7-3" title="Randomized Circular" @update-code="setCode"/>
                    </el-col>
                    <el-col :span="5">
                        <SampleProjectButton id="7-4" title="Wave Creator" @update-code="setCode"/>
                    </el-col>
                </el-row>
            </el-tab-pane>
        </el-tabs>
    </div>

</template>

<script>
    import SampleProjectButton from './SampleProjectCard'

    export default {
        data() {
            return {
                name: "SampleProjectArea",
                activeName: '1',
                tabPosition: 'left'
            }
        },
        methods: {
            setCode: function(code){
                this.$emit('set-code', code);
            }
        },
        components: {
            'SampleProjectButton': SampleProjectButton,
        },
    }
</script>

<style scoped>

</style>
