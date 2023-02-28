<div class="login_wrap">
    <Weather class="weather"></Weather>
    <div class="form_wrap">
       
        <el-form
            ref="formRef"
            :model="loginData"
            label-width="100px"
            class="demo-dynamic"
        >
        <Weather class="weather"></Weather>
            <el-form-item
                prop="username"
                label="用户名"
                :rules="[
                    {
                    required: true,
                    message: '此项为必填项',
                    trigger: 'blur',
                    }, 
                ]"
            >
                <el-input v-model="loginData.username" />
            </el-form-item>
            
            <el-form-item
                prop="password"
                label="密码"
                :rules="[
                {
                required: true,
                message: '此项为必填项',
                trigger: 'blur',
                }, 
            ]"
            >
                <el-input type="password" v-model="loginData.password" />
            </el-form-item>
        </el-form>
        <el-button type="primary" class="login_btn" @click="handleLogin">登录</el-button>
        <!-- <p>{{num}}</p> -->
    </div>
</div>
