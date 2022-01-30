<template>
    <div id="page">
                        <div class="logo">CoderBot</div>
<div class="subtitle">archivio aggiornamenti</div>
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
                    <template v-if="updatePackages.length > 0">
                    <h3>Pacchetti di aggiornamento</h3>
                    <p style="color:#606266"> Questi pacchetti devono essere scaricati localmente e poi caricati sull'applicazione di CoderBot in <i> Impostazioni -> Aggiornamenti </i></p>
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
                    </template>
                    
                    <h3>Varie</h3>
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
                    <br><br>
                    <h3>Immagini SD complete</h3>
                    <p style="color:#606266"> Queste immagini permettono il ripristino completo della micro SD. Devono essere <i> flashate </i> sulla microSD utilizzata su CoderBot.</p>
                    <el-table :data="images" style="width: 100%">
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
        <small style="color:#909399"> &copy; 2019 - 2022<a href="https://coderbot.org" target="_blank">CoderBot</a> contributors. <a href="https://github.com/coderbotorg/repo" target="_blank"> Source</a>.</small>
    </div>
</template>
<script>
export default {
    data() {
        return {
            misc: [{
                date: '2019-1-8',
                name: 'Programma tag AR',
                fileName: 'program_demo_ar.json',
                downloadUrl: 'https://drive.google.com/open?id=1V3jsb6fR3ReF2SH_G0UieWPrBf_T8QoW',
                details: "Questo file deve essere importato dall'applicazione di CoderBot. Scaricarlo e poi su Coderbot: Programma -> Importa e seleziona il file appena scaricato."
            },{
                date: '2019-1-8',
                name: 'AT tag stampabili',
                fileName: 'AR-Tags.pdf',
                downloadUrl: 'https://docs.google.com/presentation/d/19ihXcSqUKD1YsvXHiZJ57-mUUR1DQKcN7kNHCHfq3dM/edit?usp=sharing',
                details: 'Stampare in formato A3 (consigliato)'}
            ],
            images: [{
                date: '2019-02-03',
                name: 'CoderBot base image 3.0 GA',
                fileName: 'coderbot_3_0_GA_20190203.img.gz',
                downloadUrl: 'https://drive.google.com/uc?id=17GYtXryAxE2Db88K_6adBmteGNMvVGKZ&export=download',
                details: 'Contiene l\'intera immagine con tutto il software aggiornato al 3 Febbraio.'
            },{
                date: '2020-08-03',
                name: 'CoderBot base image 4.0 GA',
                fileName: 'coderbot_4_0_GA_20200803.img.gz',
                downloadUrl: 'https://drive.google.com/uc?id=1QvLbWUgZjFBgNz6DWG8KuLA9lRPBuXr6&export=download',
                details: 'Contiene l\'intera immagine con tutto il software aggiornato al 3 Agosto. [versione definitiva per CoderBot con HW v5.0]'
            },{
                date: '2022-01-02',
                name: 'CoderBot base image 4.1 GA',
                fileName: 'coderbot_4_1_GA_20220102.img.gz',
                downloadUrl: 'https://drive.google.com/uc?id=1-hlXGKEZrUaLakXzBZ9G1aPkw_CCmkfS&export=download',
                details: 'Contiene l\'intera immagine con tutto il software aggiornato al 2 Gennaio. [versione definitiva per CoderBot con HW v5.0]'
            }],
            updatePackages: [{
                date: '2022-01-02',
                name: 'Add Music and IO extensions',
                fileName: 'coderbot_update_4_1_0.tar',
                downloadUrl: 'https://drive.google.com/uc?id=1QfhikwaMGniCZ7Bp-3Dd7VQh12ujomJd&export=download',
                details: 'Installs Music and IO extensions'
            }
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
