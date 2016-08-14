
Ҫ�����е�ĳ����Ŀ��ʼ�� Git ����ֻ�赽����Ŀ���ڵ�Ŀ¼��ִ�У�
$ git init

�����ǰĿ¼���м����ļ���Ҫ����汾���ƣ���Ҫ���� git add ������� Git ��ʼ����Щ�ļ����и��٣�Ȼ���ύ��

$ git add *.c
$ git add README
$ git commit -m 'initial project version'

Ҫȷ����Щ�ļ���ǰ����ʲô״̬�������� git status �������ڿ�¡�ֿ�֮������ִ�д�����ῴ�����������������
$ git status
On branch master
Changes not staged for commit:
  (use "git add <file>..." to update what will be committed)
  (use "git checkout -- <file>..." to discard changes in working directory)

        modified:   README.md

no changes added to commit (use "git add" and/or "git commit -a")

Git ֻ�����ݴ��������� git add ����ʱ�İ汾����������ύ����ô�ύ�������ע��ǰ�İ汾�����ǵ�ǰ����Ŀ¼�еİ汾�����ԣ�������git add ֮���������޶����ļ�����Ҫ�������� git add �����°汾�����ݴ�����

����ĳЩ�ļ�:
$ cat .gitignore
*.[oa]
*~


# ��Ϊע�� �C ���� Git ����
*.a       # �������� .a ��β���ļ�
!lib.a    # �� lib.a ����
/TODO     # ����������Ŀ��Ŀ¼�µ� TODO �ļ��������� subdir/TODO
build/    # ���� build/ Ŀ¼�µ������ļ�
doc/*.txt # ����� doc/notes.txt �������� doc/server/arch.txt


�ύ����:
ÿ��׼���ύǰ������git status ���£��ǲ��Ƕ����ݴ������ˣ�Ȼ���������ύ���� git commit��
$ git commit



����ʹ���ݴ�����:
����ʹ���ݴ�����ķ�ʽ���Ծ���׼��Ҫ�ύ��ϸ�ڣ�����ʱ����ô�����Է�����Git �ṩ��һ������ʹ���ݴ�����ķ�ʽ��ֻҪ���ύ��ʱ�򣬸� git commit ����-a ѡ�Git �ͻ��Զ��������Ѿ����ٹ����ļ��ݴ�����һ���ύ���Ӷ����� git add ���裺
$ git status
# On branch master
#
# Changed but not updated:
#
#	modified:   benchmarks.rb
#
$ git commit -a -m 'added new benchmarks'
[master 83e38c7] added new benchmarks
 1 files changed, 5 insertions(+), 0 deletions(-)


�Ƴ��ļ�:
Ҫ�� Git ���Ƴ�ĳ���ļ����ͱ���Ҫ���Ѹ����ļ��嵥���Ƴ���ȷ�е�˵���Ǵ��ݴ������Ƴ�����Ȼ���ύ�������� git rm ������ɴ�������������ӹ���Ŀ¼��ɾ��ָ�����ļ��������Ժ�Ͳ��������δ�����ļ��嵥���ˡ�
\$ git rm grit.gemspec
rm 'grit.gemspec'
���ɾ��֮ǰ�޸Ĺ������Ѿ��ŵ��ݴ�����Ļ��������Ҫ��ǿ��ɾ��ѡ�� -f����ע���� force ������ĸ�����Է���ɾ���ļ���ʧ�޸ĵ����ݡ�

�ƶ��ļ�
���������� VCS ϵͳ��Git ���������ļ��ƶ������������ Git ����������ĳ���ļ����ֿ��д洢��Ԫ���ݲ��������ֳ�����һ�θ������������� Git �ǳ������������ƶϳ�����������ʲô�����ھ�������������ģ������Ժ���̸��

��Ȼ��ˣ����㿴�� Git �� mv ����ʱһ���������ѡ�Ҫ�� Git �ж��ļ�������������ô����
$ git mv file_from file_to


�޸����һ���ύ
��ʱ�������ύ���˲ŷ���©���˼����ļ�û�мӣ������ύ��Ϣд���ˡ���Ҫ�����ղŵ��ύ����������ʹ�� --amend ѡ�������ύ��
$ git commit --amend

����ղ��ύʱ�����ݴ�ĳЩ�޸ģ������Ȳ����ݴ������Ȼ�������� --amend �ύ��
$ git commit -m 'initial commit'
$ git add forgotten_file
$ git commit --amend
�����������������ֻ�ǲ���һ���ύ���ڶ����ύ���������˵�һ�����ύ���ݡ�


���Զ�ֿ̲�
Ҫ���һ���µ�Զ�ֿ̲⣬����ָ��һ���򵥵����֣��Ա㽫�����ã����� git remote add [shortname] [url]��

�������ݵ�Զ�ֿ̲�
��Ŀ���е�һ���׶Σ�Ҫͬ���˷���Ŀǰ�ĳɹ������Խ����زֿ��е��������͵�Զ�ֿ̲⡣ʵ��������������ܼ򵥣� git push [remote-name] [branch-name]�����Ҫ�ѱ��ص� master ��֧���͵�origin �������ϣ��ٴ�˵���£���¡�������Զ�ʹ��Ĭ�ϵ� master �� origin ���֣�������������������
$ git push origin master


�鿴Զ�ֿ̲���Ϣ
���ǿ���ͨ������ git remote show [remote-name] �鿴ĳ��Զ�ֿ̲����ϸ��Ϣ������Ҫ������¡�� origin �ֿ⣬�������У�

�½���ǩtag:

�½���ǩ
Git ʹ�õı�ǩ���������ͣ��������ģ�lightweight���ͺ���ע�ģ�annotated������������ǩ�����Ǹ�����仯�ķ�֧��ʵ���������Ǹ�ָ���� ���ύ��������á�������ע��ǩ��ʵ�����Ǵ洢�ڲֿ��е�һ�������������������У�����Ϣ�������ű�ǩ�����֣������ʼ���ַ�����ڣ��Լ���ǩ˵������ ǩ����Ҳ����ʹ�� GNU Privacy Guard (GPG) ��ǩ�����֤��һ�����Ƕ�����ʹ�ú���ע�͵ı�ǩ���Ա㱣�������Ϣ����Ȼ�����ֻ����ʱ�Լ�ע��ǩ�����߲���Ҫ��ע������Ϣ������������ǩҲû���⡣

����ע�ı�ǩ
����һ������ע���͵ı�ǩ�ǳ��򵥣��� -a ����ע��ȡ annotated ������ĸ��ָ����ǩ���ּ��ɣ�

ǩ���ǩ
��������Լ���˽Կ���������� GPG ��ǩ���ǩ��ֻ��Ҫ��֮ǰ�� -a ��Ϊ -s ����ע�� ȡ signed ������ĸ�����ɣ�
$ git tag -s v1.0 -m 'my signed 1.0 tag'

��������ǩ
��������ǩʵ���Ͼ���һ�������Ŷ�Ӧ�ύ�����У�����Ϣ���ļ���Ҫ���������ı�ǩ��һ�� -a��-s �� -m ѡ����ã�ֱ�Ӹ�����ǩ���ּ��ɣ�
$ git tag v1.0

��֤��ǩ
����ʹ�� git tag -v [tag-name] ����ע��ȡ verify ������ĸ���ķ�ʽ��֤�Ѿ�ǩ��ı�ǩ������������ GPG ����֤ǩ������������Ҫ��ǩ���ߵĹ�Կ������� keyring �У�������֤��
$ git tag -v v1.10


�����ǩ
Ĭ������£�git push ������ѱ�ǩ���͵�Զ�˷������ϣ�ֻ��ͨ����ʽ������ܷ����ǩ��Զ�˲ֿ⡣�������ʽ��ͬ���ͷ�֧������git push origin [tagname] ���ɣ�
$ git push origin v1.0
Counting objects: 1, done.
Writing objects: 100% (1/1), 181 bytes | 0 bytes/s, done.
Total 1 (delta 0), reused 0 (delta 0)
To https://github.com/MariShunxiang/GitTrainning.git
 * [new tag]         v1.0 -> v1.0

���Ҫһ���������б��������ı�ǩ��ȥ������ʹ�� --tags ѡ�











