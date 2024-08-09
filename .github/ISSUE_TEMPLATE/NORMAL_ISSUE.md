name: 问题报告
description: "如果需要反馈 Bug,请使用这个模板。"
labels: ["BUG"]
body:
  - type: textarea
    id: description
    attributes: 
      label: 问题描述
      description: 在下方的编辑框描述你的问题
      placeholder: |
        请**尽可能简单并全面的**描述问题。
        勿使用例如“主管！！！主管！！！” “大佬” “搞快点”这类词汇。
        滥用反馈功能可能导致被列入黑名单或是被封禁。
    validations:
      required: true
  - type: dropdown
    id: type
    attributes: 
      label: 问题类型
      description: |
    选择问题类型
    **诸如刷物品等恶性漏洞，请直接私聊管理员！**
      options: 
        - 材质问题（例如材质包，家具，实体显示异常，这类问题请确定你使用了最新的材质包）
        - 数值问题（某个数值未按预期工作，例如占位符（像%abc_defg%这样的）没有正常显示）
        - 权限问题（例如一个应该可以被玩家执行的命令未给予权限）
        - 流程问题（例如对话出现错乱，死循环）
        - 游戏客户端问题（例如崩溃）
        - 其他
    validations:
      required: true
  - type: textarea
    id: serverlog
    attributes: 
      label: 服务端日志
      description: |
        如果出现崩溃等问题，填写latest.log
        如果日志超出字数限制，请在 https://mclo.gs/ 上传日志文件，在下方填写链接。
        你还可以提供截图和文件（可以直接利用QQ的Ctrl+Alt+A截图后，Ctrl+V粘贴到这个框，或者拖动文件）
      render: text
    validations:
      required: false
  - type: checkboxes
    id: agrees
    attributes:
      label: 协议
      description: 问题反馈条款
      options:
        - label: 我确认在最新版的阈限天际服务器，这个 issue 仍然没有被解决。
          required: true
        - label: 我已经在群聊搜索过并寻找其他人，以检查是否有人已经有了解决方案。
          required: true
        - label: 我查阅了所有其他 issues，并已经确认我的问题不是重复的。
          required: true
        - label: 我已知情并同意：需要正确填写 issues 格式，否则此反馈将会被直接锁定。
          required: true
        - label: 我已知情并同意：如果滥用 issues 功能，我可能被列入黑名单甚至导致被封禁。
          required: true
        - label: 我确认我没有仔细阅读随便勾选的这些选项。
          required: false
        - label: 我已认真的填写了所有必须的表单选项并正确的描述了它们。
          required: true
