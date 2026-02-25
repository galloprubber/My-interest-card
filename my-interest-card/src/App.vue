<template>
    <div class="card-container">
        <div class="card" :class="{ 'dark-card': isDarkMode }">
            <!-- 姓名和职业 -->
            <h1 class="name">韩昊润</h1>
            <p class="title">软件工程·大二</p>

            <!-- 个人简介 -->
            <p class="bio">
                热爱编程、运动和音乐。正在探索前端开发的魅力，期待用创意和代码创造有趣的产品。
            </p>

            <!-- 兴趣标签 -->
            <div class="tags">
                <span class="tag">#icpc</span>
                <span class="tag">#前端</span>
                <span class="tag">#骑行</span>
                <span class="tag">#足球</span>
                <span class="tag">#跑步</span>
                <span class="tag">#音乐</span>
                <span class="tag">#游戏</span>
            </div>

            <!-- 分割线 -->
            <div class="divider"></div>

            <!-- 点赞和主题切换区域 -->
            <div class="actions">
                <button class="like-button">
                    <span class="like-icon">❤️</span>
                    <span class="like-count">0</span>
                </button>

                <button class="theme-button">
                    <span class="theme-icon">🌙</span>
                    <span>深色模式</span>
                </button>
            </div>
        </div>
    </div>
</template>

<script setup>
// 后续添加响应式
</script>

<style scoped>
/*居中排列*/
.card-container {
    width: 100%;
    padding: 20px;
    display: flex;
    justify-content: center;
    align-items: center;
}

.card {
    max-width: 400px;
    width: 100%;
    background-color: white;
    border-radius: 24px;
    padding: 32px 24px;
    box-shadow: 0 10px 40px rgba(0, 0, 0, 0.1);
    transition: all 0.3s ease;
}

/*深色卡片*/
.dark-card {
    background-color: #2d2d2d;
    color: #ffffff;
    box-shadow: 0 10px 40px rgba(0, 0, 0, 0.3);
}

.avatar-text {
    color: white;
    font-size: 36px;
    font-weight: bold;
}

.name {
    font-size: 28px;
    font-weight: bold;
    text-align: center;
    margin-bottom: 8px;
}

.title {
    font-size: 16px;
    color: #666;
    text-align: center;
    margin-bottom: 16px;
}

.dark-card .title {
    color: #aaa;
}

.bio {
    font-size: 15px;
    line-height: 1.6;
    color: #444;
    text-align: center;
    margin-bottom: 24px;
    padding: 0 8px;
}

.dark-card .bio {
    color: #ddd;
}

.tags {
    display: flex;
    flex-wrap: wrap;
    gap: 12px;
    justify-content: center;
    margin-bottom: 24px;
}

.tag {
    padding: 6px 16px;
    background-color: #f0f2f5;
    border-radius: 30px;
    font-size: 14px;
    color: #333;
    transition: all 0.2s ease;
}

.dark-card .tag {
    background-color: #404040;
    color: #fff;
}

.tag:hover {
    transform: translateY(-2px);
    box-shadow: 0 5px 15px rgba(102, 126, 234, 0.3);
    background-color: #667eea;
    color: white;
}

.divider {
    height: 1px;
    background-color: #e0e0e0;
    margin: 20px 0;
}

.dark-card .divider {
    background-color: #404040;
}

.actions {
    display: flex;
    justify-content: space-around;
    gap: 16px;
}

.like-button,
.theme-button {
    flex: 1;
    padding: 12px 0;
    border: none;
    border-radius: 30px;
    font-size: 16px;
    font-weight: 500;
    cursor: pointer;
    display: flex;
    align-items: center;
    justify-content: center;
    gap: 8px;
    transition: all 0.2s ease;
}

.like-button {
    background-color: #ff6b6b;
    color: white;
}

.like-button:hover {
    background-color: #ff5252;
    transform: scale(1.02);
}

.theme-button {
    background-color: #f0f2f5;
    color: #333;
}

.dark-card .theme-button {
    background-color: #404040;
    color: #fff;
}

.theme-button:hover {
    background-color: #e0e0e0;
    transform: scale(1.02);
}

.dark-card .theme-button:hover {
    background-color: #505050;
}

.like-icon,
.theme-icon {
    font-size: 18px;
}
</style>
