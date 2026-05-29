# Age of Wizardry 项目说明

这是 Victoria 3 的 **Age of Wizardry** Mod 项目。

## 核心工作规范

- **总是先查阅本项目资料库 `vic3-kb/`**，找到类似实现、语法说明或规范依据后，才能进行实现。
- 如果要修改某类 Victoria 3 Mod 内容，优先查阅对应文档，例如：
  - 建筑：`vic3-kb/wiki/Building_modding.md`
  - 商品：`vic3-kb/wiki/Goods_modding.md`
  - 生产方式：`vic3-kb/wiki/Building_modding.md`、`vic3-kb/wiki/Modifier_modding.md`
  - 本地化：`vic3-kb/wiki/Localization.md`、`vic3-kb/wiki/Mod_translation.md`
  - GUI：`vic3-kb/wiki/Interface_modding.md`、`vic3-kb/wiki/GUI_script.md`
  - 法律、利益集团、科技、决议等：查阅 `vic3-kb/wiki/` 下对应 `*_modding.md` 文件。
- 实现前应搜索项目内已有类似文件，尽量沿用现有写法、命名风格和组织方式。
- 如果 `vic3-kb/` 和项目现有实现冲突，先说明冲突，再按用户确认的方向修改。

## 项目结构

- `common/`：Victoria 3 mod 脚本定义。
- `gfx/`：图标、贴图、加载图等资源。
- `gui/`：UI 定义。
- `localization/`：本地化文本。
- `.metadata/metadata.json`：Paradox mod 元数据。
- `readme.txt` / `读我.txt`：Steam Workshop 描述文本。
- `vic3-kb/`：Victoria 3 Modding 资料库，修改前必须查阅。
- `工作区/`：素材、参考、处理中内容；除非明确要求，不要随意改动。

## 开发约定

- 本项目主要支持 Victoria 3 `1.13.*`。
- 修改本地化时，通常需要同时维护英文与简体中文。
- 不要大范围重排或格式化无关文件。
- 尽量保持改动小而明确。
- 新增定义时，注意避免与原版和本 Mod 已有 key 冲突。
- 改动完成后，优先使用搜索检查引用、key、本地化是否匹配。

## 推荐工作流程

1. 明确用户要改动的系统或文件类型。
2. 查阅 `vic3-kb/` 中对应资料，必要时也查阅项目现有类似实现。
3. 总结将采用的规范或参照实现。
4. 再进行文件修改。
5. 修改后检查相关引用、本地化和命名一致性。
6. 每次修改完成后，必须在回复末尾列出「需要用户验证的内容」清单，包括需要测试的功能点、可能出问题的语法、边界情况等。
