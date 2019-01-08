<template>
    <div id="page">
                        <div class="logo">CoderBot</div>
<div class="subtitle">files repository</div>
<br> <br>
        <el-row>
            <el-col :xs="{span:0}" :span="4" hidden-md-and-down>
                <div class="grid-content"></div>
            </el-col>
            <el-col :xs="{span:24}" :span="16">
                <div class="grid-content">
                    <!--
                    <h4>SD Card Images</h4>
                    
                    <el-table :data="images" style="width: 100%">
                        <el-table-column type="expand">
                            <template slot-scope="props">
                                Includes: {{ props.row.details }}
                            </template>
                        </el-table-column>
                        <el-table-column prop="date" label="Data">
                        </el-table-column>
                        <el-table-column prop="name" label="Nome">
                        </el-table-column>
                        <el-table-column prop="fileName" label="File">
                        </el-table-column>
                        <el-table-column prop="download" label="Download">
                            <template slot-scope="scope">
                                <a :href="scope.row.downloadUrl" target="_blank" class="el-icon-download" style="font-size:32px"></a>
                            </template>
                        </el-table-column>
                    </el-table>
                    <br><br>
                -->
                    
                    <h3>Update Packages</h3>
                    <p style="color:#606266"> These packages must be downloaded and then uploaded to the CoderBot in <i>Settings -> Update</i>. </p>
                    <el-table :data="updatePackages" style="width: 100%">
                        <el-table-column type="expand">
                            <template slot-scope="props">
                                {{ props.row.details }}
                            </template>
                        </el-table-column>
                        <el-table-column prop="date" label="Data" width="140">
                        </el-table-column>
                        <el-table-column prop="name" label="Nome">
                        </el-table-column>
                        <el-table-column prop="fileName" label="File">
                            <template slot-scope="scope">
                                <pre>{{scope.row.fileName}}</pre>
                            </template>
                        </el-table-column>
                        <el-table-column prop="download" label="Download" width="90">
                            <template slot-scope="scope">
                                <a :href="scope.row.downloadUrl" target="_blank" class="el-icon-download" style="font-size:32px"></a>
                            </template>
                        </el-table-column>
                    </el-table>
                    <br><br>
                    <h3>Miscellanea</h3>
                    <el-table :data="misc" style="width: 100%">
                        <el-table-column type="expand">
                            <template slot-scope="props">
                                {{ props.row.details }}
                            </template>
                        </el-table-column>
                        <el-table-column prop="date" label="Data" width="140">
                        </el-table-column>
                        <el-table-column prop="name" label="Nome">
                        </el-table-column>
                        <el-table-column prop="fileName" label="File">
                            <template slot-scope="scope">
                                <pre>{{scope.row.fileName}}</pre>
                            </template>
                        </el-table-column>
                        <el-table-column prop="download" label="Download" width="90">
                            <template slot-scope="scope">
                                <a :href="scope.row.downloadUrl" target="_blank" class="el-icon-download" style="font-size:32px"></a>
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
        <small style="color:#909399"> &copy; 2019 CoderBot contributors. <a href="https://github.com/coderbotorg/repo"> Source </a> </small>
    </div>
</template>
<script>
export default {
    data() {
        return {
            misc: [{
                date: '2019-1-8',
                name: 'AR program',
                fileName: 'program_demo_ar.json',
                downloadUrl: 'https://drive.google.com/open?id=1V3jsb6fR3ReF2SH_G0UieWPrBf_T8QoW',
                details: 'This file must be imported from the CoderBot software. Download this file, then on CoderBot: Program -> Import and select the downloaded file.'
            },{
                date: '2019-1-8',
                name: 'Printable AR Tags',
                fileName: 'AR-Tags.pdf',
                downloadUrl: 'https://docs.google.com/presentation/d/19ihXcSqUKD1YsvXHiZJ57-mUUR1DQKcN7kNHCHfq3dM/edit?usp=sharing',
                details: 'Print this document in A3 format.'}
            ],
            images: [{}],
            updatePackages: [{
                date: '2018-12-28',
                name: '3.0.1 Release Candidate 1',
                fileName: '3.0.1-RC1-r5.tar',
                downloadUrl: 'https://github.com/CoderBotOrg/backend/releases/download/3.0.1-rc1/3.0.1-RC1-r5.tar',
                details: 'Updates Backend to bc38f28, Frontend to CoderBotOrg/vue-app@5d03c94. New Python3 dependencies (included as installed wheels, in site-packages path): cachetools (py2-py3-any wheel). Mobile net tensorflow CNN Models.'
            },
            ]
        }
    },
    methods: {}
}
</script>
<style>
.logo {
    font-size: 60px;
    font-family: 'Overpass Mono';
    font-weight: 600;
    letter-spacing: -5px;
    background-color: #070300;
    color: transparent;
    text-shadow: 3px 3px 3px rgba(255, 255, 255, 0.25);
    -webkit-background-clip: text;
    -moz-background-clip: text;
    background-clip: text;
}
.subtitle {
    color: #606266;
    font-size: 30px;
    font-family: 'Overpass Mono';
    font-weight: 600;
    letter-spacing: -4px;
    margin-top: -20px;
}
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