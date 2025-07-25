

# 第一章：理解构建 AI 产品的基础设施和工具

奠定坚实的基础是理解任何事物的关键部分，而**人工智能**（**AI**）产品的前沿看起来就像我们的宇宙一样：不断扩展。随着我们深入探索一种新的方式来构思产品、组织和我们所参与的行业，这种扩展速度每年都在加快。几乎我们生活的各个方面都将以某种方式受到 AI 的影响，我们希望阅读这本书的人能对他们支持或希望在未来构建的产品中的 AI 应用有更多信心。

本书的*第一部分*将作为对整体情况的概述。我们将涵盖术语、基础设施、AI 算法的类型以及做得好的产品，到本节结束时，你将理解在尝试构建 AI 策略时需要考虑的各种因素，无论你是打算创建一个原生 AI 产品，还是为现有产品添加 AI 功能。

管理 AI 产品是一个高度迭代的过程，产品经理的工作是帮助你的组织发现最佳的基础设施、培训和部署工作流程的组合，以最大化在目标市场中的成功。AI 产品的性能和成功在于理解管理 AI 管道所需的基础设施，管道的输出将被集成到产品中。在本章中，我们将涵盖从数据库到工作台，再到部署策略和你可以用来管理 AI 项目的工具，以及如何评估产品的有效性。

本章将作为*第一部分*后续章节的高级概述，但最重要的是为术语提供定义，这在今天市场营销主导的 AI 竞争环境中是相当困难的。现在，似乎每个产品都是 AI 产品，市场营销部门总是喜欢随便撒上这个标签，导致它几乎失去了作为描述词的意义。我们猜测这种情况不会很快改变，但消费者和客户对 AI、机器学习（ML）和数据科学的能力和具体内容有了更多的了解，我们应该能看到产品的构建和优化变得更加清晰。理解 AI 的背景对于任何考虑构建或支持 AI 产品的人来说都很重要。

本章将涵盖以下主题：

+   定义 – 什么是 AI，什么不是 AI

+   ML 与 DL – 理解两者的区别

+   ML 中的学习类型

+   顺序 – 最佳流程是什么，每个过程的环节都在哪里？

+   DB 101 – 数据库、数据仓库、数据湖和湖仓

+   管理项目 – IaaS

+   部署策略 – 我们应该如何处理这些输出？

+   在 AI 中取得成功 – 管理良好的 AI 公司如何正确管理基础设施

+   AI 的前景 – AI 将带领我们走向何方？

# 定义 – 什么是 AI，什么不是 AI

在 1950 年，数学家和二战英雄艾伦·图灵在他的论文《计算机器与智能》中提出了一个简单的问题 - *机器能思考吗？*。今天，我们仍在探讨同样的问题。根据不同的看法，AI 可以是很多东西。互联网上存在许多地图，从在医疗和金融领域使用的专家系统到面部识别，再到自然语言处理和回归模型。在继续本章内容时，我们将涵盖适用于市场新兴产品的 AI 的许多方面。

对于跨行业产品中应用 AI 的目的，在本书中，我们将主要关注在各种容量中使用的 ML 和深度学习（DL）模型，因为这些通常在任何营销能力中提到 AI。我们将使用 AI/ML 作为一个总称来涵盖一系列 ML 应用程序，我们将涵盖大多数人会考虑到的 ML 的主要领域，如 DL、计算机视觉、自然语言处理和面部识别。这些是大多数人在行业中会遇到的应用 AI 的方法，熟悉这些应用程序将为任何希望进入 AI 领域的产品经理提供帮助。如果有的话，我们希望帮助那些希望从其他产品管理背景扩展到该领域的人们选择最吸引他们的 AI 领域。

我们还希望涵盖什么是 ML 和什么不是 ML。我们能够尽可能简单地表达它：如果一台机器正在从某些过去的行为中学习，并且它的成功率因此而提高，那么它就是 ML！*学习是活跃的元素*。没有模型是完美的，但我们从使用模型中学到了很多。每个模型都会有一些超参数调整的元素，并且每个模型的使用将产生某些性能结果。与这些模型一起工作的数据科学家和 ML 工程师将能够基准性能，并看到性能如何提高。如果有一些固定的、硬编码的规则不改变，那就不是 ML。

AI 是计算机科学的一个子集，所有的程序员都在有效地做同样的事情：给计算机一组指令让其执行。如果你的当前程序在任何方式上都不从过去学习，如果它只是按照硬编码的指令执行，我们不能称之为 ML。你可能听说过*基于规则的引擎*或*专家系统*这些术语在其他程序中被提及。它们被认为是 AI 的形式，但它们不是 ML，因为尽管它们是 AI 的一种形式，但这些规则实际上是复制了一个人的工作，而系统本身并没有自行学习或改变。

我们正处于一个 AI 采用的棘手时期，在线上很难找到关于什么构成*人工智能*的准确信息。营销人员热衷于给他们的产品加上 AI 标签，但市场上仍然没有一个明确的标准来解释这一标签意味着什么。这进一步让消费者和技术人员对 AI 这一术语产生困惑。如果你对这些术语感到困惑，尤其是当它们被应用到你在网上看到的产品时，你绝对不是一个人。

另一个令人困惑的领域是“人工智能”这一总称。对大多数人来说，人工智能的概念让人联想到 1980 年代的*终结者*系列电影以及其他未来主义的、无法避免的技术毁灭描绘。虽然人工智能确实可能带来很多伤害，但这种描绘代表的是所谓的*强人工智能*或**通用人工智能**（**AGI**）。我们距离 AGI 还有很长的路要走，但我们已经拥有了很多所谓的**狭义人工智能**或**狭义 AI**（**ANI**）。

ANI 通常也被称为*弱人工智能*，当你看到 AI 标签出现在你在网上找到的产品上时，它通常指的就是这个。ANI 就是字面意思：一种狭窄的 AI 应用。它也许擅长和你对话，预测某些未来的数值，或者整理事务；也许它在这方面是专家，但它的专长不会扩展到其他领域。如果它能扩展到其他领域，它就不再是 ANI 了。AI 的这些主要类别被称为强人工智能和弱人工智能，是与人类智能相比的。即使是最具说服力的对话 AI，虽然它们非常逼真，也只是表现出一种虚幻的智能。实际上，现有的所有 AI 都是弱人工智能或 ANI。我们的*终结者*时代仍然遥不可及，也许永远不会实现。

对于每个曾经看到关于 AI 具有自我意识或对我们抱有恶意的 Reddit 讨论的人，我们想要明确声明：AGI 并不存在，也没有所谓的具有自我意识的 AI。这并不意味着 AI 在其当前形式下不会主动并常规地对人类造成伤害。这里的一个重要警告是，不道德、草率的 AI 应用已经在积极地给我们带来小的麻烦和大的困扰。伦理和负责任地构建 AI 仍然是一个进行中的工作。虽然 AI 系统可能不会有意识地策划人类的灭亡，但当它们未经测试、不当管理，并且在偏见上没有经过充分审查时，已经部署的 ANI 应用确实能够在我们的生活中造成真正的伤害。

目前，机器能像我们一样思考吗？不，它们并不像我们一样思考。它们将来会吗？我们希望不会。个人而言，我认为人类境遇中的无法忍受的方面应该随着我们结束。但我们确实相信，我们将经历一些最大的痛苦，以及一些最狂野的好奇心，这些都会在人工智能和机器学习的善意影响下产生深远的影响。

# ML 与 DL — 理解它们的区别

作为产品经理，你需要与技术团队建立深厚的信任，以便一起构建一个在技术上表现最佳的优秀产品。如果你正在阅读本书，你很可能已经遇到过“ML”和“DL”这两个词。我们将在以下章节中使用*ML*和*DL*这两个标题来讲解一些基础知识，但请记住，我们将在*第三章*进一步阐述这些概念。

## ML

在其基本形式中，**ML** 由两个基本组成部分构成：*使用的模型* 和 *其学习的数据*。这些数据是历史数据点，有效地为机器提供了学习的基础，每次重新训练模型时，模型理论上都在不断改进。如何选择、构建、调整和维护模型以优化性能是数据科学家和 ML 工程师的工作。将这些性能优化应用于产品体验本身则是产品经理的工作。如果你在 AI 产品管理领域工作，你将与数据科学和 ML 团队紧密合作。

我们还想区分一下作为 AI 产品经理时你将与哪些人合作。根据你的组织结构，你可能是在与数据科学家和开发者合作以部署 ML，或者你是在与 ML 工程师合作，他们不仅可以训练和维护模型，还能将其部署到生产环境中。我们强烈建议与所有这些相关团队（包括 DevOps 团队）保持良好的关系。

所有的 ML 模型都可以分为以下四大类：

+   监督学习

+   无监督学习

+   半监督学习

+   强化学习

这些是机器学习（ML）的四个主要领域，每个领域都有其特定的模型和算法，用于各自的专业化方向。学习类型与是否对数据进行标注以及你用来奖励模型以获得良好表现的方法有关。这些学习类型无论你的产品是否使用深度学习（DL）模型，都与之相关，因此它们适用于所有 ML 模型。我们将在后面的章节中更深入地讨论学习类型，标题为*机器学习中的学习类型*。

## DL

**DL**是机器学习（ML）的一个子集，但这些术语在口语中常常几乎被当作独立的表达使用。原因在于，深度学习基于神经网络算法，而机器学习可以被看作是…其余的算法。在前面涵盖机器学习的部分中，我们查看了如何获取数据，利用这些数据训练模型，并使用训练好的模型预测新的未来数据点。每次你使用这个模型时，你可以通过了解误差率来看到它离正确答案有多远，从而进行反复迭代，直到得到一个足够有效的模型。每次，你都是基于包含某些模式或*特征*的数据创建一个模型。

这个过程在深度学习（DL）中是相同的，但深度学习的一个关键区别在于，数据中的模式或特征主要是通过深度学习算法通过所谓的**特征学习**或**特征工程**在分层系统中被捕捉到。我们将在接下来的部分深入探讨各种算法，因为每种算法之间有一些细微差别，但随着你不断发展对机器学习（ML）类型的理解，你也会开始将构成这些主要 AI 领域（ML 和 DL）的不同模型进行分组。出于营销目的，你会大多数看到诸如*ML*、*DL/神经网络*或只是通用的*AI*等术语，用来指代使用 DL 算法的地方。

了解这些术语在实践和模型层面的含义，并且了解它们是如何被非技术性利益相关者传达的，这一点非常重要。作为产品经理，我们处于两个世界的交界处：工程部门在构建的东西和营销部门在传达的内容。每当你听到**黑箱模型**这个术语时，它指的就是神经网络模型，也就是深度学习。原因在于深度学习工程师通常无法确定他们的模型是如何得出某些结论的，这就造成了对模型操作的不可见性。这种不可见性是双重的，既对工程师和技术人员自身来说如此，也对下游的客户和用户来说也是如此，他们正在体验这些模型的效果，却不知道模型是如何做出某些决定的。深度学习神经网络模仿的是人类思考的结构，使用多层神经网络的方式。

对于产品经理来说，深度学习（DL）带来了可解释性的问题，因为我们对模型是如何得出结论的几乎没有了解，并且根据产品的具体情况，可解释性的重要性可能会有所不同。另一个固有的挑战是，这些模型本质上是自我学习的，因为它们不会等待工程师选择对数据最相关的特征；神经网络本身会进行特征选择。它几乎不需要工程师的输入就能学习。可以把这些模型看作是*“做什么”*，而接下来的学习类型部分则是*“如何做”*。再次提醒，当我们继续讨论学习风格时（无论是监督学习、无监督学习、半监督学习还是强化学习），这些学习风格适用于深度学习（DL）和传统的机器学习（ML）模型。

让我们来看一下机器学习中的不同学习类型。

# 机器学习中的学习类型

在本节中，我们将介绍监督学习、无监督学习、半监督学习和强化学习之间的区别，以及这些学习类型如何应用。再次强调，学习类型与是否对数据进行标注以及你用来奖励模型良好表现的方法有关。最终目标是理解哪种学习模型能带来你所需的性能和可解释性，从而帮助你在决定是否将其应用到产品中时做出选择。

## 监督学习

如果人类在标注数据，并且机器也在寻找正确标注当前或未来数据点，那么这是监督学习。因为我们人类知道机器正在试图得出的答案，我们可以看到它们与正确答案的偏差，然后我们不断训练模型并进行再训练，直到我们找到一个满意的准确度。

监督学习模型的应用包括分类模型，例如垃圾邮件过滤器，用于将数据进行分类；或回归模型，用于找出变量之间的关系，以预测未来事件并发现趋势。请记住，所有模型只会在一定程度上有效，这也是它们需要不断训练和更新的原因，因此 AI 团队通常会使用集成建模，或尝试多种模型并选择表现最好的一个。无论哪种方式，它都不完美，但通过足够的辅导，它会让你越来越接近真相。

以下是你在生产中可能会使用的常见监督学习模型/算法的列表，这些模型可用于各种产品：

+   **朴素贝叶斯分类器**：该算法*天真地*将数据集中的每个特征视为独立变量。因此，它本质上是通过概率方式寻找关联，而不对数据做任何假设。它是所有算法中较为简单的之一，正是其简单性使得它在分类问题中如此成功。它通常用于二元值的问题，例如判断某个内容是否为垃圾邮件。

+   **支持向量机**（**SVM**）：该算法也主要用于分类问题，基本上是将数据集划分为两个类别，以便你可以将数据分组并预测未来数据点在这些主要划分中的位置。如果数据之间的分组不明显，SVM 允许你添加更多维度，从而更容易看到分组。

+   **线性回归模型**：这些模型自 1950 年代以来就已经存在，是我们解决回归问题（如预测未来数据点）时最简单的模型。它们本质上使用数据集中的一个或多个变量来预测因变量。该模型中的*线性*部分试图找到最佳拟合数据的直线，这条直线决定了预测的方式。在这里，我们再次看到一个相对简单的模型，因为它的多功能性和可靠性使得它被广泛使用。

+   **逻辑回归**：该模型与线性回归类似，你有独立变量和因变量，但它并不是预测一个数值，而是预测未来的二元分类状态，例如预测某人未来是否会违约。

+   **决策树**：该算法在预测分类问题和数值问题时都表现良好，因此被广泛用于这两类机器学习问题，例如预测未来的状态或价格。虽然这种方法较少见，但决策树常用于这两类问题，这也促成了它的流行。与树的比较来自于它的节点和分支，这些节点和分支就像流程图一样运作。该模型通过学习过去数据的流向来预测未来的值。

+   **随机森林**：该算法是在前述决策树的基础上构建的，且同样用于分类和数值问题。其工作原理是将数据拆分为不同的*随机*“样本”，为每个样本创建决策树，然后根据平均值或多数投票来做出预测（具体取决于你是用它进行分类还是数值预测）。由于随机森林的推理过程较难理解，如果对可解释性要求不是特别高，可以使用它。

+   **K-最近邻**（**KNNs**）：该算法专门用于分类和数值预测，因此它寻找未来的状态，并提供按组分配的结果。组内的数据点数量由工程师/数据科学家设定，模型的工作方式是通过对数据进行分组，确定数据与其邻居共享的特征，并基于这些邻居给出对未来值的最佳猜测。

现在我们已经讨论了监督学习，接下来让我们讨论无监督学习。

## 无监督学习

如果数据没有标签，并且我们正在使用机器来给数据加标签并发现我们尚未了解的模式，那就是无监督学习。实际上，我们人类要么知道正确答案，要么不知道，这就是我们区分机器学习算法属于哪个类型的方式。正如你可能想象的那样，我们对无监督学习模型的结果持有一些怀疑态度，因为它可能找到的模式并不实际有用或准确。无监督学习模型还需要大量数据来进行训练，因为如果它尝试从小样本数据中寻找模式，结果可能会非常不准确。随着它接收更多的数据，性能将逐步提高并变得更加精确，但再次强调，这没有*正确*的答案。

无监督学习模型的应用包括聚类和降维。聚类模型将数据分割或分组到某些区域。这些可以用于诸如在医学试验或药物发现中寻找模式的任务，因为你正在寻找可能尚无明显答案的数据连接和数据组。降维本质上是去除数据集中那些对你想要的性能贡献较小的特征，从而简化数据，使得最重要的特征能够最佳地提高性能，从噪声中区分出真实的信号。

以下是你在生产环境中可能会使用的常见无监督学习模型/算法列表：

+   **K-means 聚类**：该算法将数据点分组，以便更好地发现模式（或簇），同时也会寻找某个最优的簇数。这是无监督学习，因此模型试图找到可以从中学习的模式，因为它没有获得任何来自使用它的工程师的提示或监督。而且，分配的簇数是一个超参数，你需要选择最优的簇数。

+   **主成分分析** (**PCA**): 使用无监督机器学习对非常大的数据集进行处理时，常见的问题是存在太多不相关的数据，难以找到有意义的模式。这就是为什么 PCA 如此常用的原因，因为它是减少数据维度的好方法，同时不会丢失或舍弃任何信息。这对于大数据集特别有用，例如在基因组测序或药物发现试验中寻找模式。

接下来，让我们深入了解半监督学习。

## 半监督学习

在一个完美的世界里，我们会有大量标注良好的数据集，用于创建不会过拟合的最佳模型。**过拟合**是指你创建并调整一个模型，使其完全适应现有数据集，但它可能拟合得过于完美，这意味着它对特定的数据集进行了优化，但在面对更广泛的数据时表现不佳。这是数据科学中的一个常见问题。我们生活在一个不完美的世界中，常常会遇到数据不足或根本没有足够标注数据的情况。这时，半监督学习就派上了用场。我们提供一些标注数据集，并且还包括一个未标注的数据集，从而在模型尝试发现模式时，给它一些正确方向上的提示。

它与监督学习没有相同的绝对真理级别，但它确实为模型提供了一些有用的线索，以组织其结果，从而找到通向正确答案的更容易路径。

例如，假设你在寻找一个能够有效检测照片或语音模式的模型。你可能会标注其中的一些数据，然后观察未标注数据在性能上的改进情况。你可以在半监督学习中使用多个模型。这个过程类似于监督学习，监督学习使用标注数据集进行学习，从而准确了解它与正确答案的偏差。监督学习和半监督学习之间的主要区别是，半监督学习是在预测一部分新的未标注数据，然后基本上将其准确性与标注数据进行对比。你把未标注的新数据点加入训练集，使得它在正确数据上进行*训练*。

最后，为了结束本节内容，让我们简要了解一下强化学习。

## 强化学习

这一领域的机器学习通过试错有效地进行学习，它从过去的行为中学习，并自我调整方法以找到最佳的表现。强化学习有一个顺序，它实际上是基于权重和奖励的系统，通过奖励来强化正确的结果。最终，模型会尝试优化这些奖励，并随着时间的推移不断提高。我们看到强化学习在机器人学中得到广泛应用，例如，机器人通过训练学习如何操作并调整自身以适应现实世界中的各种不可预测性。

现在我们已经讨论并理解了不同类型的机器学习，让我们继续了解机器学习过程的最佳流程。

# 顺序——什么是最佳流程，过程中的每个环节在哪里？

想要通过 AI/ML 创造价值的公司，与其犹豫不决的竞争对手相比，有很多潜力可供挖掘。根据麦肯锡全球研究院的数据，“*到 2025 年，完全吸收 AI 到其价值创造工作流程中的公司，将在 2030 年全球经济中主导，并实现+120%的现金流增长*。” 接受并将 AI 生产化——无论是在产品中还是用于内部目的——是复杂的，技术债务沉重且昂贵的。一旦选择了模型和用例，将其实现到生产环境中成为一个难以管理的程序，这是许多公司将面临的挑战，尤其是当我们看到非科技行业的公司开始面对 AI 接纳的挑战时。将过程操作化、更新模型、保持数据的新鲜与清洁、组织实验，以及验证、测试和存储等相关工作，都是复杂的部分。

为了让整个过程更易于理解，我们将其呈现为一个逐步的流程，因为其中有不同层次的复杂性，但基本组件是相同的。一旦你完成了简单部分，并确定了你认为最适合你用例的模型和算法，你就可以开始完善你的 AI 系统管理流程。

## 第一步 – 数据可用性与集中化

本质上，你需要一个中央位置来存储你的 AI/ML 模型和算法将要学习的数据。根据你投资的数据库或使用的遗留系统，你可能需要一个 ETL 管道和数据工程，来为你的生产化 AI/ML 模型提供数据层和元数据，从而使其能够进行数据摄取并提供洞察。可以把这看作是创建供你的 AI/ML 系统使用的管道。

AI 依赖于数据，如果你的数据交付系统笨拙或缓慢，你在生产过程中会遇到问题。选择存储数据的首选方式本身就很棘手。你无法预见技术栈在扩展时会如何演变，因此选择一个既具成本效益又可靠的解决方案本身就是一个任务。例如，当我们在之前工作的网络安全公司开始为更多客户提供服务时，我们注意到某些客户面向的仪表板加载时间变慢。问题部分源于客户数量的增加，以及他们的元数据过大，无法支持我们现有的管道。

## 第二步 – 持续维护

到这个阶段，你已经有了自己的模型和算法，并且选择了一个数据传输系统。现在，你将进入持续维护这个系统的流程。在 DevOps 中，这被称为**持续集成**(**CI**)/**持续交付**(**CD**)。在后续章节中，我们将介绍**AI 操作**(**AIOps**)的概念，但目前，以下是针对 AI 管道持续维护的各个阶段的清单。以下是持续维护过程中四个主要组成部分：

+   **CI**：测试/验证代码和组件，以及数据、数据模式和模型

+   **CD**：代码的更改或更新会持续传递，因此，一旦你做出更改，它们将先出现在测试环境中，然后再进入生产环境，而不会有任何暂停。

+   **CT**：我们已经提到过，持续学习对 ML 来说非常重要，而**持续训练**将这一过程转化为生产化，以便在你的数据源被刷新时，模型能够持续训练并从新的数据中学习。

+   **CM**：我们不能让 ML/AI 模型持续运行而不**持续监控**它们，以确保没有出现严重问题。

如果你不不断迭代你的流程，你就无法负责任地管理 AI 项目。你的模型和超参数会变得陈旧。你的数据也会过时，当这种迭代过程停滞时，它将不再有效。性能是你需要不断更新的内容，因为无论是否面向客户，性能不佳都将显而易见。话虽如此，事情也可能会出错。例如，性能的滞后或模型更新频率的下降可能导致人们失业、无法获得竞争力的按揭利率，或者被判不公正的监禁。由于模型维护不当，可能会带来下游效应，从而产生严重后果。我们建议你查阅本章末尾的*附加资源*部分，获取更多示例和信息，了解停滞不前的 AI 系统如何对环境和人们造成灾难性影响。

B 101 – 数据库、数据仓库、数据湖和湖仓

AI/ML 产品依赖于数据运行。数据存储的位置和方式是一个重要的考量，它会影响你的 AI/ML 性能，在这一部分，我们将讨论一些最常见的数据存储工具。找到存储、访问和训练数据的最佳方式本身就是一个专业领域，但如果你从事 AI 产品管理，最终你需要理解使你的 AI 产品运作的基本构成要素。简单来说，就是数据。

由于 AI 需要大数据，这将成为你产品和业务的重要战略决策。如果你没有一个高效的系统，开个玩笑，你将遇到一些问题，这会影响你模型的性能，进而影响你产品本身。对你特定产品的最具成本效益且以性能为驱动的解决方案有一个清晰的把握，并在这些不同的因素之间找到平衡，将有助于你作为产品经理的成功。是的，你会依赖技术高管做出许多这样的决策，但你将参与这些决策的制定，因此在这里需要一定的了解。

让我们来看看一些用于存储 AI/ML 产品数据的不同选项。

## 数据库

根据你组织的目标和预算，你将以某种方式在数据湖、数据库和数据仓库之间集中管理数据，甚至可能会考虑一个新的选择：数据湖仓。如果你刚刚开始接触这个领域，你可能只是将数据存储在关系型数据库中，以便可以轻松访问和查询。如果你的设置相对简单，数据库是实现这一目标的好方法。使用关系型数据库时，如果你想将这些数据与另一个数据库中的数据结合，你将面临对齐这些模式的问题。

如果你主要使用数据库进行查询以访问数据，并且只使用公司数据的某一子集来分析一般趋势，那么关系型数据库可能已经足够。如果你想将来自不同领域的各种数据集结合起来，并且希望完成更高级的分析、仪表盘或 AI/ML 功能，那么你需要继续阅读。

## 数据仓库

如果你希望将数据集中存储，并且有大量结构化数据进入，你更有可能使用数据仓库。这实际上是迈向成熟的第一步，因为它能帮助你快速地从各个业务单元中提取洞察和趋势。如果你希望以多种方式利用 AI/ML，而不仅仅是某一种特定的方式，那么这将对你非常有帮助。

比如说，假设你想在现有产品中以及 HR 功能中添加 AI 特性。你将利用客户数据，根据其他同类群体的表现，向客户提供趋势或预测，同时使用 AI/ML 对内部员工进行预测或优化。这两个使用场景都可以通过数据仓库得到很好的支持。

数据仓库确实需要一些前期投资，以制定计划并设计数据结构。同时，它们也需要昂贵的投入，因为它们能够按需提供数据供分析使用，所以你需要为保持数据随时可用而支付额外费用。根据内部用户的技术水平，你可以选择更便宜的选项，但如果大多数业务用户需要容易理解的数据分析方式，这个选项对于组织来说是最优的。不管怎样，数据仓库将使你能够为内部用户和利益相关者团队创建仪表盘。

## 数据湖（和湖仓）

如果你手头有大量原始的、非结构化的数据，并且希望找到一个更具成本效益的存储地点，那么你可以考虑数据湖。在这里，你可以存储非结构化、半结构化以及结构化数据，且这些数据可以被更具技术背景的内部用户轻松访问。例如，数据科学家和机器学习工程师能够处理这些数据，因为他们会创建自己的数据模型来实时转换和分析数据，但这并非大多数公司所能做到的。

如果你的数据湖中有大量的、业务用户不需要立即使用的数据，保持数据在数据湖中的存储会非常便宜，但你永远无法真正用数据湖替代数据仓库或数据库。数据湖更像是一个“锦上添花”的选择。如果你有一个庞大的历史数据湖，计划在未来用于分析，你需要考虑另一种存储方式，以便获取那些洞察。

你可能还会遇到**湖仓**这个术语。目前市面上有许多数据库、数据仓库和数据湖。然而，我们所知道的唯一湖仓是由一家名为 Databricks 的公司推广的。它提供类似数据湖的服务，但具有一些数据仓库的功能，特别是展示数据、使数据对非技术内部用户可用且可吸收，并能用这些数据创建仪表盘。这里最大的优势在于，你可以提前存储数据并支付存储费用，同时也能在后续访问和处理这些数据。

## 数据管道

无论你使用什么技术来维护和存储数据，你仍然需要设置管道，确保数据的流动，确保你的仪表盘能根据业务需求及时刷新，并确保数据按照需要的方式流动。处理和传递数据也有多种方式。你可能会对大批量的数据进行批处理（batch processing），在不同的时间间隔移动，或者使用实时管道，在数据生成的瞬间就能获取实时数据。如果你希望利用预测分析、启用报告，或者有一个系统来移动、处理和存储数据，那么数据管道可能就足够了。然而，根据你的数据正在做什么以及需要多少转换，你很可能会同时使用数据管道，甚至更具体地使用 ETL 管道。

**ETL** 代表**提取、转换和加载**，因此你的数据工程师将为更高级的系统创建特定的管道，比如将所有数据集中到一个地方、添加数据或进行数据丰富、将数据与你的**CRM**（**客户关系管理**）工具连接，甚至在系统间转换数据并为其添加结构。这样做的原因是，当使用数据仓库或数据库时，这是一个必要的步骤。如果你仅使用数据湖，你将拥有分析所需的所有元数据，并可以根据需要获得洞察。在大多数情况下，如果你正在使用 AI/ML 产品，你将与一位数据工程师合作，帮助推动所需的数据流，确保你的产品成功，因为你很可能同时使用关系型数据库和数据仓库。使 AI/ML 功能生效所需的分析很可能需要由专注于 ETL 管道的数据工程师来支持。

管理和维护这个系统也将是你数据工程师的工作，我们鼓励每个产品经理与支持其产品的数据工程师保持密切关系。两者之间的一个关键区别是，ETL 管道通常是批量更新的，而不是实时更新的。例如，如果你使用 ETL 管道来更新客户如何使用产品的历史性日常信息，并在平台中提供面向客户的洞察，那么保持每天下午两次更新这个批量更新可能是最理想的。然而，如果你需要为内部业务用户使用的仪表盘提供实时洞察，并且他们依赖这些数据做出日常决策，那么你很可能需要依赖一个持续更新的数据管道。

现在，我们理解了存储数据的不同选项以及如何为业务选择合适的选项，接下来让我们讨论如何管理我们的项目。

# 项目管理 – IaaS

如果你打算在组织中创建 AI/ML 系统，你必须将其视为一个独立的生态系统，且需要持续维护。这也是为什么 MLOps 和 AIOps 与 DevOps 团队密切合作的原因。越来越多的我们将开始看到更多的托管服务和**基础设施即服务**（**IaaS**）产品问世。行业已经出现了向像 Determined AI 和 Google 的 AI 平台管道工具等公司转型的趋势，以满足市场需求。这个需求的核心是希望减轻那些在开始承担搭建 AI 系统这一巨大任务时感到困惑的公司的一些负担。

就像 DevOps 团队在大规模软件开发中变得流行一样，经过数十年的错误，我们也将看到类似的现象出现在 MLOps 和 AIOps 中。开发解决方案和将其投入运行是两个不同的关键领域，需要协同工作。这对于 AI/ML 系统尤其如此。当前的趋势是 IaaS。这是一个重要的概念，因为刚刚接触 AI 的公司通常不了解正确实施 AI 所需的成本、存储、计算能力和投资，特别是对于需要大量数据进行训练的深度学习（DL）AI 项目。

到目前为止，大多数公司还没有运行 AI/ML 项目数十年，也没有专门的团队。像 MAANG（Meta、Amazon、Apple、Netflix、Google）这样的科技公司在管理 AI/ML 方面引领着文化规范，但大多数需要拥抱 AI 的公司并非科技公司，而且在应对 AI 采纳所带来的技术债务方面，工程团队基本上没有准备。

为了启动 AI 项目而采取的捷径将需要对代码进行重构，或改变数据存储和管理方式，这也是为什么 AI 采纳的战略规划至关重要的原因。这也是为什么这么多 IaaS 服务不断涌现，帮助工程团队保持灵活，以便在未来需要变更时可以更方便。随着时间的推移，保持 AI 团队正常运行所需的基础设施将发生变化，使用 IaaS 提供商的优势在于，你可以运行所有项目，且只需为 AI 开发人员实际使用数据训练模型的时间付费。

# 部署策略——我们该如何处理这些输出？

一旦你对所选择的模型（包括它们的性能和错误率）感到满意，并且你的基础设施足以支持产品和选定的 AI 模型用例，你就可以准备进入流程的最后一步，将代码部署到生产环境中。保持适合你产品和组织的部署策略将是我们在上一节中提到的持续维护的一部分。你需要考虑诸如何时重新训练模型和更新训练数据以防止模型衰退和数据漂移等问题。你还需要一个系统来持续监控模型的表现，因此这个过程将非常具体，取决于你的产品和业务，特别是因为这些重新训练的周期会导致系统的一些停机时间。

部署将是一个动态的过程，因为你的模型主要是试图有效地对真实世界数据做出预测，因此，取决于你的数据所处的环境，你可能需要根据情况给予部署更多或更少的关注。例如，在我们为一家机器学习房地产科技公司工作的过程中，由于迁移数据和房价数据因疫情而发生剧烈变化，我们几乎每天都在更新、重新训练和重新部署我们的模型。如果这些模型没有得到及时检查，而且没有来自产品双方的工程师和业务领导支持（无论是客户端还是内部），我们可能无法及时发现模型在代表不充分的数据时所做的严重偏差。

你还需要了解一些著名的部署策略。我们将在以下小节中讨论它们。

## 阴影部署策略

在这种部署策略中（通常称为**阴影模式**），你将部署一个带有新特性的模型，同时保留一个已经存在的模型，这样部署的新模型仅仅作为当前生产中模型的*影像*存在。这也意味着新模型会像现有模型一样处理所有接收到的请求，但不会展示该模型的结果。此策略使你能够观察阴影模型在相同的真实世界数据上是否表现更好，而不会中断正在生产环境中运行的模型。一旦确认新模型表现更好且没有运行问题，它将成为主要模型，完全部署到生产环境中，而原有模型将被淘汰。

## A/B 测试模型部署策略

在这个策略中，我们实际上看到两个略有不同的模型，具有不同的功能，目的是同时了解它们在实际环境中的表现。这两个模型是同时设置的，并且性能已经优化，以促进转化。这实际上就像是一个实验，你在观察一个模型与另一个模型的结果，并且从一些假设或预期开始，认为某一个模型比另一个模型表现更好，然后你验证这些假设，看看自己是否是对的。然而，你的模型差异必须非常小，因为如果两个模型的特征差异过大，你就无法理解到底是什么因素让你取得了最大的成功。

## 金丝雀部署策略

在这里，我们看到了一种更渐进的部署方式，你实际上创建了一些用户子集，之后这些用户将体验你的新模型部署。在这里，我们看到被引入到新模型的用户数量随着时间的推移逐渐增加。这意味着你可以在用户群体之间有一定的缓冲时间，以了解他们是如何反应和与这个新模型互动的。本质上，你是在用不同的用户群体作为测试者，在发布到下一批用户之前，逐步发现潜在的错误。如果你有耐心和勇气，这个过程虽然缓慢，但也很有回报。

还有更多的策略可以选择，但请记住，这些策略的选择将取决于你的产品性质，最重要的是你的客户和用户的需求，还有你的预算、指标和性能监控、技术能力和知识、以及你所拥有的时间表。除了部署之外，你还需要帮助你的业务理解他们应该多频繁地进行代码重构和分支。

现在我们已经讨论了不同的部署策略，让我们来看一下成功实现 AI 所需的条件。

# 在 AI 中取得成功——管理良好的 AI 公司如何做好基础设施

这表明了机器学习系统的复杂性，许多依赖机器学习的大型科技公司都拥有专门的团队和平台，专注于构建、训练、部署和维护机器学习模型。以下是一些你在构建机器学习/人工智能程序时可以采用的选项：

+   **Databricks 有 MLflow**：MLflow 是由 Databricks 开发的开源平台，旨在帮助企业管理完整的机器学习生命周期。它允许你进行实验并与任何库、框架或语言协作。其主要优点包括实验跟踪（可以查看你的模型在不同实验之间的表现）、模型管理（管理团队成员之间的所有模型版本）、以及模型部署（可以在工具中快速查看部署情况）。

+   **Google 拥有 TensorFlow Extended (TFX)**：这是 Google 基于 TensorFlow 构建的最新产品，是一个端到端的平台，用于部署生产级别的 ML 流水线。它允许你在团队内外进行协作，并提供强大的功能，适用于可扩展的高性能环境。

+   **Uber 拥有 Michelangelo**：Uber 是一个很好的例子，他们在内部创建了自己的 ML 管理工具，用于协作和部署。此前，他们使用的是不同的语言、模型和算法，团队之间也存在孤岛现象。在实施 Michelangelo 后，他们能够将不同的技能和能力整合到一个系统中。他们需要一个可靠、可重现和标准化的流水线，用于大规模地创建、管理、预测和部署数据。

+   **Meta 拥有 FBLearner Flow**：Meta 还为管理其众多 AI 项目创建了自己的系统。由于机器学习（ML）是其产品的基础组成部分，Meta 需要一个平台来实现以下目标：

    +   每个曾经实现的 ML 算法，都要具备在以后由其他人重复使用的能力。

    +   每个工程师都应具备编写可以重复使用的训练流水线的能力。

    +   让模型训练变得简单和自动化。

    +   每个人都应该能轻松地搜索过往的项目和实验。

实际上，Facebook 创建了一个易于使用的知识库和工作流程，以集中管理他们的所有 ML 操作。

+   **Amazon 拥有 SageMaker**：这是 Amazon 的产品，允许你使用其自有的一系列完全托管的基础设施工具和工作流程来构建、训练和部署你的 ML 模型和程序。该产品的理念是根据客户的需求，提供低代码或无代码的用户界面，无论你是雇佣了 ML 工程师还是业务分析师。如果你已经在使用 Amazon 的云基础设施，那么使用他们的基础设施来自动化和标准化你的 ML/AI 项目和操作，进一步提升规模化能力，也是非常有优势的。

+   **Airbnb 拥有 Bighead**：Airbnb 创建了自己的 ML 基础设施，旨在实现 AI/ML 组织之间的标准化和集中化。他们使用了如 Zipline、Redspot 和 DeepThought 等一系列工具来协调他们的 ML 平台，力图实现与 Facebook 和 Uber 相同的目标：减少错误和差异，最小化重复性工作。

正如我们所见，有多个平台可以用来创建、训练和部署 ML 模型。最后，让我们来看看 AI 的未来将会是什么样子。

# AI 的承诺——AI 将把我们带向何方？

那么，AI 实施的时代将走向何方？这对所有行业意味着什么？目前，我们正面临一个具有地缘政治影响的行业，这是一项技术上显而易见的决策，伴随着大量责任、成本和机会。只要公司和产品经理意识到正确照顾 AI 程序所需的风险、成本和投资水平，将其作为好奇心的源泉，并将 AI/ML 应用到早期创造成功的项目中，并从这些知识中不断发展，投资于 AI 的公司将体验到 AI 的承诺。这一承诺根植于量化预测和优化。例如，Highmark Inc. 通过使用 ML 进行欺诈检测，在 2019 年节省了超过 2.6 亿美元，GE 通过预测性维护帮助客户节省了超过 16 亿美元，亚马逊的 35% 销售额来自其推荐引擎。

当三分之一的收入来自 AI 算法时，几乎没有任何反驳的余地。不管你在 AI/ML 上投资多少，确保你通过合理规划和战略来最大化其效能，找到了解该领域及其潜在风险的有能力的人才，并选择合适的可扩展基础设施，以限制重构工作。

只要你的 AI/ML 项目直接与影响成本节省或收入的结果挂钩，如果你负责这些项目，你很可能会在自己的职业生涯中获得成功。建议从小处着手，将其应用于明确的商业目标，追踪该目标，并展示其有效性，这是一种聪明的策略，因为本章详细讲述了维护 AI 程序的多个领域，以及可能遇到的障碍。 如果你无法向即使是最犹豫的高管传达 AI 的优势和能力，证明时间、人员投入和基础设施支出的价值将是一个挑战。

这对于你的技术资源（数据科学家、数据工程师和 ML 工程师）以及你的业务利益相关者也很重要。了解你将使用的 ML 算法或获得一些关于如何最好地存储数据的建议是一回事，但如果你没有与自己的项目进行迭代，增长自己的知识和直觉，去了解哪些方法最有效，你将无法真正成为组织内部变革的推动者。我们通过迭代学习，并且完成任务的成功越多，我们的信心也越大。作为产品经理，你也会有同样的经历。

在之前的例子中，GE 通过为客户提供成本节省，高马克通过预测欺诈来防止未来的瓶颈，而亚马逊则通过 ML 增加了收入。当我们思考 AI 的前景以及它将引领我们走向何方时，这些例子推动了这样一个观点：这是最新工业革命的摇篮。这不仅是对公司有益的事情，更是对所有人都将带来益处。虽然这些益处的分配可能并不完全平等，因为最终是那些投资于这项技术的公司，且它们将首先寻求获得最高回报，但要点是，消费者和企业都将从 AI 中受益。

# 总结

本章涵盖了很多内容，但请记住，这里提到的许多概念将在后续章节中进一步讨论。很难过分强调 AI/ML 成功所需的基础设施，因为其性能很大程度上取决于我们如何传递数据以及如何管理部署。我们讨论了 ML 和 DL 的基本定义，以及它们可以采用的学习类型。我们还讨论了搭建和维护 AI 管道的一些基础知识，并列举了一些其他公司如何管理此类操作的例子。

构建利用 AI/ML 的产品是一项雄心勃勃的任务，本章旨在为整体建立 AI 程序的过程提供足够的基础，这样我们就可以在接下来的章节中不必引入太多新的概念，从而在这个过程中逐步深入各个方面。如果你感到有些不知所措，那只意味着你正在掌握构建 AI 所需的规模。这是一个好兆头！在*第二章*中，我们将详细讨论如何使用和维护我们在本章中简要介绍过的 ML 模型。

# 额外资源

如需更多信息，可以参考以下资源：

+   *Weapons of Math Destruction*（《数学摧毁武器》） by Cathy O’Neil: [`www.amazon.com/Weapons-Math-Destruction-Increases-Inequality/dp/0553418815`](https://www.amazon.com/Weapons-Math-Destruction-Increases-Inequality/dp/0553418815)

)

+   *Invisible Women: Exposing Data Bias in a World Designed for Men*（《隐形女性：揭露一个为男性设计的世界中的数据偏见》） by Caroline Criado Perez: [`www.amazon.com/Invisible-Women-Data-World-Designed/dp/1419735217/ref=sr_1_1?keywords=invisible+women&qid=1673296808&sr=8-1`](https://www.amazon.com/Invisible-Women-Data-World-Designed/dp/1419735217/ref=sr_1_1?keywords=invisible+women&qid=1673296808&sr=8-1)

+   *The Ethical Algorithm: The Science of Socially Aware Algorithm Design*（《伦理算法：社会意识算法设计的科学》） by Michael Kearns, Aaron Roth: [`www.amazon.com/Ethical-Algorithm-Science-Socially-Design/dp/0190948205/`](https://www.amazon.com/Ethical-Algorithm-Science-Socially-Design/dp/0190948205/)

)

+   *人工智能误解：计算机如何误解世界* 由梅雷迪斯·布鲁萨德（Meredith Broussard）著作：[`www.amazon.com/Artificial-Unintelligence-Computers-Misunderstand-World/dp/026253701X/`](https://www.amazon.com/Artificial-Unintelligence-Computers-Misunderstand-World/dp/026253701X/)

)

+   *压迫的算法：搜索引擎如何加剧种族主义* 由萨菲亚·乌莫贾·诺布尔（Safiya Umoja Noble）著作：[`www.amazon.com/Algorithms-Oppression-Search-Engines-Reinforce/dp/1479837245/`](https://www.amazon.com/Algorithms-Oppression-Search-Engines-Reinforce/dp/1479837245/)

)

+   *技术后的种族：废奴主义工具与新的吉姆法则* 由鲁哈·本杰明（Ruha Benjamin）著作：[`www.amazon.com/Race-After-Technology-Abolitionist-Tools/dp/1509526404/`](https://www.amazon.com/Race-After-Technology-Abolitionist-Tools/dp/1509526404/)

)

+   *监控资本主义时代：新权力前沿的人类未来之战* 由肖莎娜·祖博夫（Shoshana Zuboff）著作：[`www.amazon.com/Age-Surveillance-Capitalism-Future-Frontier/dp/1541758005/`](https://www.amazon.com/Age-Surveillance-Capitalism-Future-Frontier/dp/1541758005/)

)

+   *自动化不平等：高科技工具如何剖析、监控与惩罚贫困人群* 由维吉尼亚·尤班克斯（Virginia Eubanks）著作：[`www.amazon.com/Automating-Inequality-High-Tech-Profile-Police/dp/1250074312/`](https://www.amazon.com/Automating-Inequality-High-Tech-Profile-Police/dp/1250074312/)

)

+   *数据女权主义* 由凯瑟琳·迪尼贾佐（Catherine D’Ignazio）著作：[`www.amazon.com/Feminism-Strong-Ideas-Catherine-DIgnazio/dp/0262044005/`](https://www.amazon.com/Feminism-Strong-Ideas-Catherine-DIgnazio/dp/0262044005/)

)

# 参考资料

+   [`www.canva.com/careers/topic/machine-learning/`](https://www.canva.com/careers/topic/machine-learning/)

)

+   *模型部署* *策略*：[`neptune.ai/blog/model-deployment-strategies`](https://neptune.ai/blog/model-deployment-strategies)

)

+   *人工智能助力多邻国个性化语言学习*：[`www.wired.com/brandlab/2018/12/ai-helps-duolingo-personalize-language-learning/#:~:text=The%20learning%20behind%20the%20lingo,data%20and%20make%20intelligent%20predictions`](https://www.wired.com/brandlab/2018/12/ai-helps-duolingo-personalize-language-learning/#:~:text=The%20learning%20behind%20the%20lingo,data%20and%20make%20intelligent%20predictions)

+   [`www.crunchbase.com/organization/ggwp-65c2`](https://www.crunchbase.com/organization/ggwp-65c2)

+   [`www.cbinsights.com/company/anon-ai`](https://www.cbinsights.com/company/anon-ai)

+   *AI-50 美国最具前景的人工智能公司*：[`www.forbes.com/sites/alanohnsman/2021/04/26/ai-50-americas-most-promising-artificial-intelligence-companies/?sh=3b5e27ef77cf`](https://www.forbes.com/sites/alanohnsman/2021/04/26/ai-50-americas-most-promising-artificial-intelligence-companies/?sh=3b5e27ef77cf)

+   [`www.lacework.com/labs/`](https://www.lacework.com/labs/)

+   [`www.crunchbase.com/organization/lacework/company_financials`](https://www.crunchbase.com/organization/lacework/company_financials)

+   *SHEIN 的 AI 程序匹配本地需求并实现* *规模化*： [`www.psfk.com/2022/06/sheins-consumer-to-manufacturer-ai-program-matches-local-demand-at-scale.html#:~:text=Shein’s%20AI%20engine%20can%20quickly,brand%20much%20cheaper%20operating%20costs`](https://www.psfk.com/2022/06/sheins-consumer-to-manufacturer-ai-program-matches-local-demand-at-scale.html#:~:text=Shein’s%20AI%20engine%20can%20quickly,brand%20much%20cheaper%20operating%20costs)

)

+   *产品驱动增长，* *韦斯·布什*

+   *关注差距 - 只有在生产环境中才算是 AI/ML：数据战略系列第* *4* *部分*： [`www.credera.com/insights/mind-gap-not-ai-ml-unless-production-data-strategy-series-part-4`](https://www.credera.com/insights/mind-gap-not-ai-ml-unless-production-data-strategy-series-part-4)

)

+   *Airbnb 的端到端 ML* *平台*： [`medium.com/acing-ai/airbnbs-end-to-end-ml-platform-8f9cb8ba71d8`](https://medium.com/acing-ai/airbnbs-end-to-end-ml-platform-8f9cb8ba71d8)

)

+   *Amazon* *SageMaker*： [`aws.amazon.com/sagemaker/`](https://aws.amazon.com/sagemaker/)

+   *介绍 FBLearner Flow：Facebook 的 AI* *骨干*： [`engineering.fb.com/2016/05/09/core-data/introducing-fblearner-flow-facebook-s-ai-backbone/`](https://engineering.fb.com/2016/05/09/core-data/introducing-fblearner-flow-facebook-s-ai-backbone/)

)

+   *认识米开朗基罗：Uber 的机器学习* *平台*： [`www.uber.com/blog/michelangelo-machine-learning-platform/`](https://www.uber.com/blog/michelangelo-machine-learning-platform/)

)

+   *TFX 是一个用于部署生产级 ML* *管道*的端到端平台： [`www.tensorflow.org/tfx`](https://www.tensorflow.org/tfx)

)

+   *管理的 MLflow 管理完整的机器学习* *生命周期*： [`www.databricks.com/product/managed-mlflow`](https://www.databricks.com/product/managed-mlflow)

)

+   *发现* *Lakehouse*： [`www.databricks.com/discoverlakehouse?utm_medium=paid+search&utm_source=google&utm_campaign=13039235745&utm_adgroup=125064728314&utm_content=product+page&utm_offer=discoverlakehouse&utm_ad=576656880219&utm_term=what%20is%20a%20lakehouse&gclid=CjwKCAjwx7GYBhB7EiwA0d8oe_HabROASQAaw7XYRq-VinQLswPqDyh8iPCT4032m8UN7H0B0uNyVBoCZ-QQAvD_BwE`](https://www.databricks.com/discoverlakehouse?utm_medium=paid+search&utm_source=google&utm_campaign=13039235745&utm_adgroup=125064728314&utm_content=product+page&utm_offer=discoverlakehouse&utm_ad=576656880219&utm_term=what%20is%20a%20lakehouse&gclid=CjwKCAjwx7GYBhB7EiwA0d8oe_HabROASQAaw7XYRq-VinQLswPqDyh8iPCT4032m8UN7H0B0uNyVBoCZ-QQAvD_BwE)

)

+   *计算机机械与* *智能*： [`phil415.pbworks.com/f/TuringComputing.pdf`](https://phil415.pbworks.com/f/TuringComputing.pdf)

)

+   *构建 MLOps* *基础的关键要求*： [`cloud.google.com/blog/products/ai-machine-learning/key-requirements-for-an-mlops-foundation`](https://cloud.google.com/blog/products/ai-machine-learning/key-requirements-for-an-mlops-foundation)

)

+   *TikTok 是如何使用机器* *学习的?*: [`dev.to/mage_ai/how-does-tiktok-use-machine-learning-5b7i`](https://dev.to/mage_ai/how-does-tiktok-use-machine-learning-5b7i)
