## cmd创建视图文件

1. 创建基础MVC结构视图.

		cd /path/to/MyApp
		sencha generate view foo.Thing

	The above will generate the following files:

		app/
	    view/
	        foo/                    # Folder for the classes implementing the new view
	            Thing.js            # The new view
	            ThingModel.js       # The `Ext.app.ViewModel` for the new view
	            ThingController.js  # The `Ext.app.ViewController` for the new view

2. 创建继承视图

		cd /path/to/MyApp
		sencha generate view -base Ext.container.Container foo.Thing

	Note. This command is not compatible with a Sencha Architect project.

默认创建不加模式的话，会在app目录下创建新的view，如果需要在classic或者 modern下创建，则需要添加--classic标识

3. 创建一个控制器

		cd /path/to/MyApp
		sencha generate controller Central