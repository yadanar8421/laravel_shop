<template>
    <el-menu background-color="transparent" text-color="#fff">
        <el-menu-item index="dashboard">
            <i class="el-icon-menu"></i>
            <Link :href="$route('dashboard')">Dashboard</Link>
        </el-menu-item>

        <el-menu-item index="organizations">
            <i class="el-icon-document"></i>
            <Link :href="$route('organizations.index')">Organizations</Link>
        </el-menu-item>

        <el-menu-item index="contacts">
            <i class="el-icon-setting"></i>
            <Link :href="$route('contacts')">Contacts</Link>
        </el-menu-item>

        <el-menu-item index="reports">
            <i class="el-icon-setting"></i>
            <Link :href="$route('reports')">Reports</Link>
        </el-menu-item>

        <el-submenu index="1">
            <template #title>
                <i class="el-icon-location"></i>
                <span>导航一</span>
            </template>

            <el-menu-item-group>
                <template #title>分组一</template>
                <el-menu-item index="1-1">选项1</el-menu-item>
            </el-menu-item-group>

            <el-submenu index="1-2">
                <template #title>选项2</template>
                <el-menu-item index="1-2-1">选项1</el-menu-item>
            </el-submenu>
        </el-submenu>

        <MenuActiveItemDetector />
    </el-menu>
</template>

<script>
import MenuActiveItemDetector from './MenuActiveItemDetector.vue';

export default {
    name: 'LayoutAsideMenu',
    components: { MenuActiveItemDetector },
}
</script>
