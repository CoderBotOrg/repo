<template>
    <div id="page">
        <h1> CoderBot files </h1>
        <el-row>
            <el-col :xs="{span:0}" :span="4" hidden-md-and-down>
                <div class="grid-content"></div>
            </el-col>
            <el-col :xs="{span:24}" :span="16">
                <div class="grid-content bg-purple-light">
                    <el-table :data="tableData" style="width: 100%">
                        <el-table-column type="expand">
                            <template slot-scope="props">
                                <p>Address: {{ props.row.address }}</p>
                            </template>
                        </el-table-column>
                        <el-table-column prop="date" label="Data">
                        </el-table-column>
                        <el-table-column prop="name" label="Nome">
                        </el-table-column>
                        <el-table-column prop="address" label="Download">
                            <template slot-scope="scope">
                                <a :href="scope.row.address" class="el-icon-download" style="font-size:32px"></a>
                            </template>
                        </el-table-column>
                    </el-table>
                </div>
            </el-col>
            <el-col :xs="{span:0}" :span="4" hidden-md-and-down>
                <div class="grid-content"></div>
            </el-col>
        </el-row>
        <br>
        <small> &copy; 2019 CoderBot contributors. <a href="https://github.com/coderbotorg/repo"> Source </a> </small>
    </div>
</template>
<script>
export default {
    data() {
        return {
            tableData: [{
                date: '2016-05-03',
                name: 'Tom',
                address: 'No. 189, Grove St, Los Angeles'
            }, {
                date: '2016-05-02',
                name: 'Tom',
                address: 'No. 189, Grove St, Los Angeles'
            }, {
                date: '2016-05-04',
                name: 'Tom',
                address: 'No. 189, Grove St, Los Angeles'
            }, {
                date: '2016-05-01',
                name: 'Tom',
                address: 'No. 189, Grove St, Los Angeles'
            }]
        }
    },
    methods: {}
}
</script>
<style>
a {
    text-decoration: none;
    transition: ease-out;
}

#page {
    font-family: Helvetica Neue, Helvetica, sans-serif;
    text-align: center;
}

.el-row {
    margin-bottom: 20px;

    &:last-child {
        margin-bottom: 0;
    }
}

.el-col {
    border-radius: 4px;
}

.bg-purple-dark {
    background: #99a9bf;
}

.bg-purple {
    background: #d3dce6;
}

.bg-purple-light {
    background: #e5e9f2;
}

.grid-content {
    border-radius: 4px;
    min-height: 36px;
}

.row-bg {
    padding: 10px 0;
    background-color: #f9fafc;
}
</style>