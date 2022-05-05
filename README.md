- 👋 Hi, I’m @3125878389
- 👀 I’m interested in ...
- 🌱 I’m currently learning ...
- 💞️ I’m looking to collaborate on ...
- 📫 How to reach me ...

<!---
3125878389/3125878389 is a ✨ special ✨ repository because its `README.md` (this file) appears on your GitHub profile.
You can click the Preview link to take a look at your changes.
--->
Exception
Unknown Property – yii\base\UnknownPropertyException
Getting unknown property: frontend\components\WebUser::realname
1. in /www/wwwroot/jywt.96123a.net/vendor/yiisoft/yii2/base/Component.phpat line 143
2. in /www/wwwroot/jywt.96123a.net/vendor/yiisoft/yii2/db/BaseActiveRecord.php at line 252– yii\base\Component::__get('realname')
3. in /www/wwwroot/jywt.96123a.net/frontend/modules/admin/views/layouts/main.php at line 33– yii\db\BaseActiveRecord::__get('realname')
27282930313233343536373839            <a aria-hidden="false" class="nav-toggle Hui-iconfont visible-xs" href="javascript:;">&#xe667;</a>
 
            <nav id="Hui-userbar" class="nav navbar-nav navbar-userbar hidden-xs">
                <ul class="cl">
                    <li><?= current(admin\models\AdminUser::roles(u('id'))) ?></li>
                    <li class="dropDown dropDown_hover">
                        <a href="javascript:;" class="dropDown_A"><?= u()->realname ?> <i class="Hui-iconfont">&#xe6d5;</i></a>
                        <ul class="dropDown-menu menu radius box-shadow">
                            <li><a href="javascript:;" data-title="修改密码" onclick="Hui_admin_tab(this)" _href="<?= url(['site/profile']) ?>">修改密码</a></li>
                            <?php if (u()->power <= AdminUser::POWER_ADMIN): ?>
                            <li><a href="javascript:;" data-title="个人信息" onclick="Hui_admin_tab(this)" _href="<?= url(['site/userInfo']) ?>">个人信息</a></li>
                            <?php endif ?>
                            <li><a href="<?= url(['site/login']) ?>">切换账户</a></li>
4. in /www/wwwroot/jywt.96123a.net/common/components/View.php at line 37– require('/www/wwwroot/jywt.96123a.net/fro...')
31323334353637383940414243     */
    public function renderPhpFile($_file_, $_params_ = [])
    {
        ob_start();
        ob_implicit_flush(false);
        extract($_params_, EXTR_OVERWRITE);
        require($_file_);
 
        return ob_get_clean();
    }
 
    /**
     * 快速引入css文件
5. in /www/wwwroot/jywt.96123a.net/vendor/yiisoft/yii2/base/View.php at line 247– common\components\View::renderPhpFile('/www/wwwroot/jywt.96123a.net/fro...', ['content' => ''])
6. in /www/wwwroot/jywt.96123a.net/vendor/yiisoft/yii2/base/Controller.php at line 399– yii\base\View::renderFile('/www/wwwroot/jywt.96123a.net/fro...', ['content' => ''], admin\controllers\SiteController)
7. in /www/wwwroot/jywt.96123a.net/vendor/yiisoft/yii2/base/Controller.php at line 385– yii\base\Controller::renderContent('')
8. in /www/wwwroot/jywt.96123a.net/frontend/modules/admin/controllers/SiteController.php at line 22– yii\base\Controller::render('index')
16171819202122232425262728    public function actionIndex()
    {
        $this->layout = 'main';
 
        $this->view->title = config('web_name') ? config('web_name') . ' - 管理系统' : '';
 
        return $this->render('index');
    }
 
    public function actionProfile()
    {
        return $this->render('profile');
    }
9. admin\controllers\SiteController::actionIndex()
10. in /www/wwwroot/jywt.96123a.net/vendor/yiisoft/yii2/base/InlineAction.php at line 55– call_user_func_array([admin\controllers\SiteController, 'actionIndex'], [])
11. in /www/wwwroot/jywt.96123a.net/vendor/yiisoft/yii2/base/Controller.php at line 160– yii\base\InlineAction::runWithParams([])
12. in /www/wwwroot/jywt.96123a.net/vendor/yiisoft/yii2/base/Module.php at line 454– yii\base\Controller::runAction('index', [])
13. in /www/wwwroot/jywt.96123a.net/vendor/yiisoft/yii2/web/Application.php at line 84– yii\base\Module::runAction('admin/site/index', [])
14. in /www/wwwroot/jywt.96123a.net/vendor/yiisoft/yii2/base/Application.php at line 375– yii\web\Application::handleRequest(yii\web\Request)
15. in /www/wwwroot/jywt.96123a.net/frontend/web/index.php at line 20– yii\base\Application::run()
14151617181920    require(__DIR__ . '/../../common/config/main-local.php'),
    require(__DIR__ . '/../config/main.php'),
    require(__DIR__ . '/../config/main-local.php')
);
 
$application = new yii\web\Application($config);
$application->run();
$_COOKIE = [
    '_csrf' => '1b450f337c69dbcbb21f011e87fc320c13739d358157034f33ae220ffbf7adc6a:2:{i:0;s:5:"_csrf";i:1;s:32:"Iig-YXlxOc0bThZra6kbBchW5JX4o9TU";}',
    '_identity' => 'c6e6cf5076ef6684a44a95cb35f952a885979b9a0fae5285531069f06c1f2b9da:2:{i:0;s:9:"_identity";i:1;s:14:"[1,"",2592000]";}',
    'PHPSESSID' => '2b77lrm6dglgjr96gqgflpj1m5',
];

$_SESSION = [
    '__flash' => [],
    '_formToken' => 'MUVSZ0ZRbFd4LDVKHwkAL34mYgUSOTYlUHM5BQQyBAAEDwpTKWg4Ag==',
    '__user' => 1,
];
Yii Framework
2022-05-05, 14:37:45

Apache

Yii Framework/2.0.8
