<template>
<aside class="left-side sidebar-offcanvas">
    <section class="sidebar">
        <!-- Sidebar user panel -->
        <div class="user-panel">
            <div class="pull-left image">
                <img :src="auth.avatar" class="img-circle" alt="User Image" />
            </div>
            <div class="pull-left info">
                <p>{{ auth.username }}</p>

                <a href="#">
                    <i class="fa fa-circle text-success"></i>
                    <span v-for="role in auth.roles">{{ role.display_name }}</span>
                </a>
            </div>
        </div>
        <!-- sidebar menu: : style can be found in sidebar.less -->
        <ul class="sidebar-menu">
            <li v-link="{name: 'dashboard', activeClass: 'active', exact: true}">
                <a>
                    <i class="fa fa-dashboard"></i> <span>控制台</span>
                </a>
            </li>
            <li v-link="{name: 'users', activeClass: 'active'}">
                <a>
                    <i class="fa fa-users"></i> <span>用户</span>
                </a>
            </li>
            <li v-link="{name: 'categories', activeClass: 'active'}">
                <a>
                    <i class="fa fa-tags"></i> <span>分类</span>
                </a>
            </li>
            <li v-link="{name: 'series', activeClass: 'active'}">
                <a>
                    <i class="fa fa-film"></i> <span>系列</span>
                </a>
            </li>
            <li v-link="{name: 'videos', activeClass: 'active'}">
                <a>
                    <i class="fa fa-youtube-play"></i> <span>视频</span>
                </a>
            </li>
            <li v-link="{name: 'blogs', activeClass: 'active'}">
                <a>
                    <i class="fa fa-book"></i> <span>博客</span>
                </a>
            </li>
            <li v-link="{name: 'subscribers', activeClass: 'active'}">
                <a>
                    <i class="fa fa-newspaper-o"></i> <span>订阅</span>
                </a>
            </li>

            <li v-link="{name: 'links', activeClass: 'active'}">
                <a>
                    <i class="fa fa-link"></i> <span>链接</span>
                </a>
            </li>

        </ul>
    </section>
    <!-- /.sidebar -->
</aside>
</template>

<script>
module.exports = {
    props: ['auth']
}
</script>
