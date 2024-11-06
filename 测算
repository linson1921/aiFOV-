import math

def calculate_horizontal_fov(vertical_fov, aspect_ratio):
    """
    计算水平FOV（Horizontal FOV）
    :param vertical_fov: 垂直FOV（度数）
    :param aspect_ratio: 屏幕宽高比（例如 16:9）
    :return: 水平FOV（度数）
    """
    # 将垂直FOV转换为弧度
    vertical_fov_rad = math.radians(vertical_fov)
    
    # 计算水平FOV
    horizontal_fov_rad = 2 * math.atan(math.tan(vertical_fov_rad / 2) * aspect_ratio)
    
    # 转换回度数
    horizontal_fov = math.degrees(horizontal_fov_rad)
    return horizontal_fov

def calculate_vertical_fov(horizontal_fov, aspect_ratio):
    """
    计算垂直FOV（Vertical FOV）
    :param horizontal_fov: 水平FOV（度数）
    :param aspect_ratio: 屏幕宽高比（例如 16:9）
    :return: 垂直FOV（度数）
    """
    # 将水平FOV转换为弧度
    horizontal_fov_rad = math.radians(horizontal_fov)
    
    # 计算垂直FOV
    vertical_fov_rad = 2 * math.atan(math.tan(horizontal_fov_rad / 2) / aspect_ratio)
    
    # 转换回度数
    vertical_fov = math.degrees(vertical_fov_rad)
    return vertical_fov

def main():
    print("FPS 游戏 FOV 计算器")
    
    # 选择计算方向
    choice = input("选择计算类型: \n1. 从垂直FOV计算水平FOV\n2. 从水平FOV计算垂直FOV\n请输入 1 或 2: ")
    
    if choice == '1':
        # 从垂直FOV计算水平FOV
        vertical_fov = float(input("请输入垂直 FOV（度数）: "))
        aspect_ratio = float(input("请输入屏幕宽高比 (例如 16:9 输入 16/9): "))
        horizontal_fov = calculate_horizontal_fov(vertical_fov, aspect_ratio)
        print(f"对应的水平 FOV 是: {horizontal_fov:.2f} 度")
    
    elif choice == '2':
        # 从水平FOV计算垂直FOV
        horizontal_fov = float(input("请输入水平 FOV（度数）: "))
        aspect_ratio = float(input("请输入屏幕宽高比 (例如 16:9 输入 16/9): "))
        vertical_fov = calculate_vertical_fov(horizontal_fov, aspect_ratio)
        print(f"对应的垂直 FOV 是: {vertical_fov:.2f} 度")
    
    else:
        print("无效输入，请输入 1 或 2。")

if __name__ == "__main__":
    main()
